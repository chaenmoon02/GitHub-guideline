# 기존에 알고있었던 Commit 방법: 
## 1. GitHub Desktop을 이용하여 branch와 master 사이 수정된 소스를 pull request 요청 하는 법  <br>

* commit : 'Commit'은 작업한 내용을 로컬 저장소에 저장하는 것을 말합니다. 작업한 파일의 변경 사항을 스냅샷으로 찍어서 로컬 저장소에 기록합니다.
* push : 'Push'는 로컬 저장소에 있는 변경 사항을 원격 저장소로 전송하는 작업을 말합니다. 로컬에서 원격으로 변경 사항을 업로드하는 과정입니다.
* pull request : 'Pull'은 원격 저장소의 변경 사항을 로컬 저장소로 가져오는 작업을 말합니다. 다른 사람이나 자신이 작업한 내용을 로컬로 가져와서 확인하고 이를 자신의 작업에 반영할 때 사용됩니다.



예시) chaenmoon02/Commit-Merge-TEST라는 repository를 생성했습니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/39e0a30d-53b8-4124-8654-a9c5b769d178)  
* master (main) 계정은 chaenmoon02이며, collaborator는 branch moon이라는 가상의 researcher를 만들었습니다. branch moon에게 새로운 branch와 collaboraotor 자격을 주었습니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/ed381e6a-136f-4c51-b6f6-3d0087a8c52e)  
*어두운 모드 : main / 밝은 모드 : branch*    

① GitHub Desktop에 접속하여 'Clone a repository from the Internet...' 버튼을 클릭합니다. 이때, researcher 시점에서 진행됩니다. (branch moon)  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/ad9381ec-a9ad-494a-94cb-eed5e3ca4aac)  

② 소스를 수정할 repository 항목을 누르고 'Clone' 버튼을 클릭합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/9cf5390f-b8c7-4d0a-81f4-aab1366c729d)  

③ branch를 부여 받은 신분이므로 본인의 branch에 commit하기 위하여 상단 'Current branch'에서 branch-moon 항목을 선택한 후 'Open in Visual Studio Code'를 클릭합니다.  
main에다가 바로 commit 해버리면 master의 원본 작업물과 공동작업자가 작성한 작업물이 꼬일 수 있기 때문입니다. 이후에 pull request를 통하여 merge 즉, 코드를 정리된 상태로 합쳐야 합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/9085f111-e2e3-47ed-9e13-2c3f2ce76ff7)  

④ branch moon 계정에서 9~12번 초록색으로 강조된 부분이 추가 및 수정된 부분입니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/f782514c-0392-4bad-aceb-376b4a9394b4)  

⑤ Visual Studio Code에서 Ctrl + S 단축키를 이용하여 저장하면, 자동으로 GitHub Desktop에서 수정된 부분이 보입니다. 이후, 'Commit to **branch-moon**' 버튼을 클릭하고 'Push origin' 버튼도 클릭합니다. 이 기능을 통해 github branch로 정상적으로 commit됩니다. 저장 개념과 동일하게 볼 수 있습니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/bfe1a723-ecba-46c1-963b-fa504170cd64)  
 

⑥ main branch에 공동작업자가 수행한 작업물을 병합하기 위하여 Pull request 요청 보내는 과정이 필요합니다. branch moon 계정 GitHub에 자동적으로 'Compare & pull request' 버튼이 활성화됩니다. (**branch-moon** had recent pushes 2 seconds ago)  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/1c1eb084-4dc7-4529-98b7-a5d2caeb4eea)  
main master에게 설명을 덧붙여 요청을 전송할 수 있습니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/d0cd733e-37af-461a-a067-642410be5555)  

## 2. Pull request 요청 수락 및 Merge 하는 방법  

① main master (chaenmoon02) 시점입니다. 'Pull requests' 목록에 branch moon first commit 제목의 요청을 확인할 수 있습니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/09653e05-f332-45f7-aabd-9146330808c0)    
branch researcher에게 전송받은 전달 사항입니다.    
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/04272f0a-6d12-4865-a3be-6cf16b9f1a90)   

② 'Merge pull request', 'Confirm merge' 순서로 클릭해줍니다.   
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/e6f6adbc-d5e7-4d9d-b28d-f27444746ee5)  

정상적으로 merge 된 모습입니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/8931cdb7-02c8-4f0d-a77c-9d0f6b612a52)  
*왼쪽 : main master / 오른쪽 : researcher branch*  

## 3. branch와 main merge 하는 동안 발생할 수 있는 문제 : "Merge 충돌 관리"  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/72184b6f-98e7-4d18-b6fa-7798700e81ce)  
왼쪽 작업물은 branch에서 편집한 작업물로, 제대로 merge 반영이 되어있습니다. 그러나 오른쪽 작업물인 main 작업물에서는 위의 merge가 제대로 반영이 되어 있지 않은 채로 각자 작업물이 편집되어 있는 상황입니다. 이렇게 될 경우, main과 branch, branch들 간의 merge 충돌이 일어나 더욱 복잡해질 것입니다.  

```  
branch moon : 바이오소재공학연구실 한경국립대학교  
commit test  


- - -  
[finish practice]  
biolab HKNU  
second revision (master)  
```  

**따라서 작업물 동기화 과정이 필요합니다.**  

아래 사진은 main branch의 Visual Studio code 작업물입니다.  
① 동기화를 위하여 '…', 'Terminal', 'New Terminal' 순으로 클릭합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/0225a698-c8c7-4e73-a2c6-6dd236aa6bd8)  
② 'git add.'을 입력합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/c82b68d7-cc0b-415a-ae83-fc1e15f6c636)  
③ 'git commit -m "second commit"'을 입력합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/ab78b59f-385e-4767-96b5-e38154c7b409)  
④ 'git pull origin main'을 입력합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/c8d8a5c5-2d9f-4698-8598-fe17dd80ad1b)  
정상적으로 편집된 모든 과정이 업데이트됩니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/da5a3f67-e637-45b0-9639-411f8300e0a5)  
⑤ 'git push origin main'을 최종적으로 입력합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/792cd1b7-e1c0-469d-bec2-ab9312a10b9c)  
⑥ 앞서 언급했듯이, commit 하기 위해서 Ctrl + S 단축키 통해 저장 후, GitHub Desktop으로 돌아와 'Commit to main' 버튼과 Push origin' 버튼을 순서대로 클릭합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/50fad73e-b7dd-4464-920f-2ad2ef86ce5d)  

**최종적으로 main과 branch 양측의 편집된 작업물이 올바르게 merge 반영 되어있는 것을 확인할 수 있습니다.**  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/2934eec4-3541-4cd0-85af-0bddb5ef1ba5)  
*위 : branch / 아래 : main*  
- - -  


## I. Visual Studio  
Visual Studio는 Microsoft에서 개발한 통합 개발 환경입니다. 다양한 프로그래밍 언어와 플랫폼을 지원합니다.  
##### 1. Visual Studio 설치하는 법  
① Visual Studio 홈페이지에 접속해 프로그램을 다운받습니다.  
https://visualstudio.microsoft.com/ko/downloads/   
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/758b5c70-7544-4a24-9b13-20a17cee28d2)  

##### 2. 로그인  
① Sign in to Sync Settings 버튼을 눌러 로그인합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/8d8d914c-722d-4161-9f12-a315f03679ac)  

② 회원가입을 하는 대신, GitHub와 연동하여 이 프로그램을 사용할 수 있습니다. Authorize Visual-Studio-Code 버튼을 눌러 계정끼리 연동합니다.  
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/bc6ee53b-689a-47f1-bc73-0968717724aa)    

##### 3. 확장 프로그램: Extensions 탭을 눌러 필요한 확장 프로그램을 설치합니다.  
1) Prettier  
Prettier는 코트 포맷터 중 하나로서, 주로 JavaScript, HTML 등의 코드를 자동으로 포맷팅해주는 도구입니다. 코드를 일관된 스타일로 정렬하고 조정하며 코드의 가독성을 향상시키고 일관된 형식을 유지할 수 있습니다.  
2) WSL  
Windows Subsystem for Linux의 약자로, Microsoft Windows 운영 체제에서 Linux 바이너리를 실행하기 위한 호환성 계층입니다. 개발자들은 Windows 시스템 내에서 Linux 명령 및 도구를 사용할 수 있습니다.  

![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/af4619d4-f331-472b-9d0e-1d0ff612e92e)  ![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/ad0e88c7-b282-4441-82bb-c07a48c3dce1)  

## II. Commite in Github to Github 

### 1. Summarize how to commite

![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320578/5ad6c0d5-54ff-4e1a-9836-20e526c64350)
<br>

지금까지는,,,
1. Master 로 부터 Researcher 들이 정보를 다운로드.
2. 이후 VS code로 Clone을 형성하여 작업.
3. 다시 Git을 통하여 Master의 repository로 Push.

**하지만**
<br>

지금부터 설명할 새로운 방법 :  <br>
1. Master가 열어준 Branch에서 작업.
2. 다시 Master의 repository로 commite. <br>
<br>

### 1. Master 가 열어준 Branch에서 작업 하는 방법. 

#### 1-1. Master의 Repository로 들어온 모습
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320727/937a3382-3cb4-4478-8484-9fca132eae0e) <br>

#### 1-2. Master의 Repository 내의 Researcher's branch로 들어가 Researcher가 작업할 workspace가 있는 해당 파일까지 찾은 모습
![image](https://github.com/chaenmoon02/GitHub-guideline/assets/145320727/6797b662-c52e-419f-bbdb-952e037c3162)

#### 1-3. 

