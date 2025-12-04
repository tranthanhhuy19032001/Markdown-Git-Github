# Git-Github

### Mục lục
[I. Mở đầu](#Modau)

[II. Ngôn ngữ Markdown](#ngonngumarkdown)
	
[III. Các thao tác với git và github](#cacthaotacvoigitvagithub)
- [1. Initialize project](#initializeproject)
- [2. Git basic (regularly)](#gitbasic)
- [3. Git reset)](#gitreset)
- [4. Git amend)](#gitamend)
- [5. Git revert)](#gitrevert)
- [6. Git merge (regularly))](#gitmerge)
- [7. Git debase)](#gitdebase)

===========================

<a name="Modau"></a>
## I. Mở đầu
- TODO
<a name="ngonngumarkdown"></a>
## II. Ngôn ngữ Markdown

Ngôn ngữ này khá đơn giản, bạn có thể đọc tại [đây](http://daringfireball.net/projects/markdown/syntax) để biết cách sử dụng.

Nhưng với tôi, tôi không dùng hết từng ấy thứ cho nên tôi chỉ nhớ một số cái tôi hay dùng, cách tôi dùng như sau:

Tạo một file có tên bất kỳ với đuôi .md. Có thể dùng `notepad`, `notepad++`, `vi`, `nano`,... hay bất cứ thứ gì mà bạn muốn.

Một số phương pháp tôi hay sử dụng để viết:

<a name="thetieude"></a>
### 1. Thẻ tiêu đề

Markdown sử dụng kí tự # để bắt đầu cho các thẻ tiêu đề, có thể dùng từ 1 đến 6 ký tự # liên tiếp. Mức độ riêu đề giảm dần từ 1 đến 6

Tùy mục đích và ý thích bạn có thể sử dụng cách này để thể hiện các chỉ mục khác nhau.

Ví dụ:

```
# 1.Tiêu đề cấp 1
```

# 1.Tiêu đề cấp 1

```
## 2.Tiêu đề cấp 2
```

## 2.Tiêu đề cấp 2

```
###### 6.Tiêu đề cấp 6
```

###### 6.Tiêu đề cấp 6

<a name="chenlinkchenanh"></a>
### 2. Chèn link, chèn ảnh

Để chèn hyperlink bạn chỉ cần paste luôn linh đó vào file .md

```
https://github.com
```

https://github.com

Hoặc bạn cũng có thể sử dụng cú pháp sau để thu ngắn đường dẫn của link

```
[Github](https://github.com)
```

Kết quả là:

[Github](https://github.com)

Để chèn ảnh thì bạn hãy sử dụng cú pháp sau:

```
<img src="link_anh_cua_ban">
```

Tôi thường sử dụng công cụ [Lightshot](https://app.prntscr.com/en/index.html) để chụp ảnh màn hình và up hình đó lên trang http://i.imgur.com/ để lấy đường dẫn ảnh đưa vào Github

Hai công cụ này khá dễ sử dụng, bạn chỉ cần chụp màn hình bằng Lightshot ấn Ctrl + C để copy và Ctrl + V để paste vào trình duyệt tại trang web http://i.imgur.com/

<a name=kytuindaminnghieng></a>
### 3. Ký tự in đậm, in nghiêng

- Để in đậm một đoạn text  bạn chỉ cần làm như sau:

```
**từ cần in đậm**
```

**từ cần in đậm**

- Để in nghiên một đoạn text  bạn chỉ cần làm như sau:

```
*từ cần in nghiêng*
```

*từ cần in nghiêng*

<a name="trichdanbochu"></a>
### 4. Trích dẫn, bo chữ

Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

```
`đoạn cần bo`
```

Kết quả là: `đoạn cần bo`

Để làm nổi bật một đoạn, chẳng hạn như một đoạn shell hay file cấu hình bạn có thể sử dụng cú pháp như ví dụ sau:

    ```sh
    auto eth0
    iface eth0 inet static
    ipaddress 10.10.10.10
	netmask 255.255.255.0
	gateway 10.10.10.1
	dns-nameservers 8.8.8.8
    ```

Kết quả như sau:

```sh
auto eth0
iface eth0 inet static
ipaddress 10.10.10.10
netmask 255.255.255.0
gateway 10.10.10.1
dns-nameservers 8.8.8.8
```

<a name="gachdaudong"></a>
### 5. Gạch đầu dòng

Để sử dụng gạch đầu dòng bạn chỉ cần sử dụng cú pháp sau:

```
- Gạch đầu dòng thứ nhất
  
  - Thụt với đầu dòng 1
  
  - Thụt với đầu dòng 1
 
- Gạch đầu dòng thứ hai
  
  - Thụt với đầu dòng 2
  
  - Thụt với đầu dòng 2
  
```

- Gạch đầu dòng thứ nhất
  
  - Thụt với đầu dòng 1
  
  - Thụt với đầu dòng 1
  
- Gạch đầu dòng thứ hai
  
  - Thụt với đầu dòng 2
  
  - Thụt với đầu dòng 2
  

<a name="taobang"></a>
### 6. Tạo bảng

Bạn có thể sử dụng cú pháp sau để tạo bảng:

```
| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |
```

Kết quả:

| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |

<a name="meo"></a>
###*Mẹo:*

- Sử dụng trang http://markdownlivepreview.com/ paste vào đó đoạn markdown bạn viết và xem trước để chỉnh sửa cho phù hợp.

- Bạn cũng có thể sử dụng những đoạn markdown của người khác đã viết trước để tham khảo.

Như vậy bạn đã có thể trình bày github của mình một cách sáng sủa bằng markdown.

<a name="cacthaotacvoigitvagithub"></a>
## III. Các thao tác với Git và Github
<a name="initializeproject"></a>
### 1. Initialize project
<a name="gitbasic"></a>

- 1.1. Create a new repository on the command line
```
echo "# initialize_repository" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/tranthanhhuy19032001/initialize_repository.git `change your reposioty url`
git push -u origin main
```
- 1.2. OR push an existing repository from the command line
```
git remote add origin https://github.com/tranthanhhuy19032001/initialize_repository.git
git branch -M main
git push -u origin main
```
### 2. Git basic (regularly)
<a name="gitreset"></a>
### 3. Git reset
 - 3.1. Git reset
      - Đầu tiên, sử dụng lệnh git reset để đặt HEAD của bạn về commit commit_id:
        ```
          git reset --hard [commit_id]
        ```
        OR
        ```
          git reset --soft [commit_id]
        ```
    - Lệnh này sẽ loại bỏ các commit trước của commit_id và đặt HEAD tại commit_id
    - `Sự khác nhau giữa --hard và --soft:`
        - --hard: Nó sẽ đặt lại HEAD về commit cụ thể và loại bỏ tất cả các thay đổi trong Index và thư mục làm việc. Các thay đổi chưa commit sẽ mất đi mà không có cơ hội khôi phục. Điều này có nghĩa là tất cả các thay đổi chưa commit (các commit ở trạng thái "Unstaged" và "Staged") sẽ mất đi và lịch sử sẽ được làm mới.
        - --soft: Ngược lại, với --soft, HEAD được đặt lại vào commit cụ thể, nhưng thay đổi chưa commit vẫn được giữ nguyên trong Index. Điều này có nghĩa là bạn có thể thực hiện lại commit ngay lập tức nếu bạn muốn, và tất cả các thay đổi sẽ được thêm vào commit mới.
- 3.2. Git Push
  - Nếu dùng --hard:
      ```
        git push --force origin your_branch
      ```
  - Nếu dùng --soft
      ```
        git push origin your_branch
      ```

<a name="gitamend"></a>
### 4. Git amend
  - 4.1. Giữ nguyên comment log của commit
    ```
      git commit --amend --no-edit
    ```
  - 4.2. Thay đổi comment mới
    ```
      git commit --amend -m "A new comment"
    ```
<a name="gitrevert"></a>
### 5. Git revert
- Revert the commit.
- Once you have the commit hash, use the git revert command followed by the commit hash.
  ```
    git revert <commit-hash>
  ```

- If you are reverting the last commit and know it's the HEAD of your current branch, you can use HEAD as a shorthand:
```
    git revert HEAD
```
- Git will then open a text editor to allow you to edit the commit message for the new revert commit. You can accept the default message or modify it to provide more context. Save and close the editor to complete the revert. Resolve any conflicts (if necessary).

<a name="gitmerge"></a>
### 6. Git merge (regularly)
```
git checkout destination_branch_name
git merge source_branch_name
```
<a name="gitdebase"></a>
### 7. Git debase
