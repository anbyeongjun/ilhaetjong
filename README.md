<p align="center"><img src="images/ilhaetjong.png" width="128" alt="일했종? 종 아이콘"></p>

<h1 align="center">일했종?</h1>

<p align="center">업무에 집중하다 시간대별 근무 확인을 놓치지 않게, 소리 없이 알려 주는 Windows 프로그램<br>만든 사람 양천구 안병준</p>

## 받는 곳

여기가 일했종?의 공식 배포처입니다.

> [!CAUTION]
> 공식 주소 외의 파일은 실행을 권하지 않아요.<br>
> 이외의 곳에서 받은 파일을 실행했을 때 발생하는 문제는 책임지지 않습니다.

## 알아 두세요

- 앱에는 인터넷 통신 기능이 아예 없습니다.
- 설치 없이 실행 파일 하나로 동작하고, 기록은 그 PC에만 저장합니다.
- 사용 방법은 앱 위쪽 막대의 사용 방법에서 볼 수 있어요.
- 이 저장소에는 공식 실행 파일만 올립니다.

## 받은 파일이 공식 파일인지 확인하기

- 이 페이지에서 직접 받았다면 그대로 쓰시면 됩니다.
- 다른 곳에서 받았다면 그 파일은 지우고 이 페이지에서 다시 받으세요.

**직접 확인하려면**

<!-- verify:start -->
```powershell
Add-Type -AssemblyName System.Windows.Forms; $f = New-Object System.Windows.Forms.OpenFileDialog -Property @{ Title = '받은 일했종 파일을 고르세요'; InitialDirectory = "$env:USERPROFILE\Downloads"; Filter = '실행 파일 (*.exe)|*.exe' }; if ($f.ShowDialog((New-Object System.Windows.Forms.Form -Property @{ TopMost = $true })) -eq 'OK') { if ((Get-FileHash -LiteralPath $f.FileName -Algorithm SHA256).Hash -eq '7A73C934F52E5FB8DF1D78F525C84C8EDE5E7F80420A51C0F02FF4B39BDCCBB9') { Write-Host '공식 파일이 맞습니다.' -ForegroundColor Green } else { Write-Host '공식 파일이 아닙니다. 실행하지 말고 공식 페이지에서 다시 받으세요.' -ForegroundColor Red } }
```
<!-- verify:end -->

1. 위 회색 칸 오른쪽 위의 복사 버튼을 누릅니다.
2. 키보드의 Windows 키와 X를 함께 누르고 '터미널'을 누릅니다.
3. 터미널 창에 Ctrl+V로 복사한 내용을 붙여 넣은 뒤 Enter를 누릅니다.
4. 파일 고르기 창이 뜨면 받은 일했종 파일을 고릅니다.
5. "공식 파일이 맞습니다"가 나오면 됩니다. "공식 파일이 아닙니다"가 나오면 실행하지 마세요.

이 명령은 고른 파일의 값(SHA-256)을 계산해 공식 값과 비교만 합니다.<br>
이 페이지가 아닌 곳에서 알려 준 명령은 붙여 넣지 마세요.