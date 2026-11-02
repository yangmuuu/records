```sh
notepad $PROFILE


function proxy {
    $env:HTTP_PROXY = "http://127.0.0.1:10808"
    $env:HTTPS_PROXY = "http://127.0.0.1:10808"
    $env:ALL_PROXY = "socks5://127.0.0.1:10808"
    Write-Host "Proxy enabled" -ForegroundColor Green
}

function unproxy {
    Remove-Item Env:HTTP_PROXY -ErrorAction SilentlyContinue
    Remove-Item Env:HTTPS_PROXY -ErrorAction SilentlyContinue
    Remove-Item Env:ALL_PROXY -ErrorAction SilentlyContinue
    Write-Host "Proxy disabled" -ForegroundColor Yellow
}

. $PROFILE
```
