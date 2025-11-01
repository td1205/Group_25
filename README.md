💰 Celo Micro-Savings Platform DApp 💰

Đây là một Ứng dụng Phi tập trung (DApp) Micro-Savings được xây dựng trên mạng lưới Celo, nhằm thúc đẩy tài chính toàn diện bằng cách cung cấp các cơ hội tiết kiệm an toàn và dễ tiếp cận bằng stablecoin (cUSD).

I. Giới thiệu Dự án (Project Overview)

Mục tiêu

Chi tiết

Mạng lưới

Celo (Alfajores Testnet)

Smart Contract

MicroSavings.sol (Solidity 0.8.0)

Token sử dụng

cUSD (Celo Stablecoin)

Mục đích

Cho phép người dùng gửi tiền tiết kiệm nhỏ, phi tập trung và kiếm lợi nhuận (lãi suất mô phỏng).

Tóm tắt Nhiệm vụ (Mission Summary)

Nhiệm vụ cốt lõi của chúng tôi là tận dụng blockchain Celo để tạo ra một cơ chế tiết kiệm kỹ thuật số an toàn, rào cản thấp và dễ tiếp cận trên toàn cầu. Chúng tôi hướng tới việc thúc đẩy tài chính toàn diện bằng cách trao quyền cho người dùng di động xây dựng và bảo vệ tài sản cá nhân bằng tiền tệ phi tập trung, ổn định. Dự án này đóng vai trò là một minh chứng quan trọng (proof-of-concept) cho việc áp dụng rộng rãi hơn các giải pháp DeFi trong nền kinh tế di động.

II. Khắc phục Vấn đề (The Problem Solved)

Nhiều người dùng ở các thị trường mới nổi thiếu quyền truy cập vào các công cụ tiết kiệm truyền thống đáng tin cậy. Các giải pháp hiện có thường có phí cao, yêu cầu tập trung và dễ bị ảnh hưởng bởi biến động tiền tệ địa phương. DApp này cung cấp một giải pháp thay thế minh bạch, chi phí thấp và chống lạm phát bằng cách sử dụng cUSD.

III. Hướng Dẫn Triển Khai (Deployment Guide)

Dự án này được thiết lập để triển khai bằng Remix IDE và ví MetaMask.

1. Cấu hình MetaMask

Bạn phải thêm Celo Alfajores Testnet vào MetaMask.

Trường

Giá trị

Network Name

Celo Alfajores

New RPC URL

https://alfajores-forno.celo-testnet.org

Chain ID

44787

Currency Symbol

CELO

Block Explorer URL

https://alfajores.celoscan.io

Nhận Token: Lấy CELO (cho phí gas) và cUSD (để tiết kiệm) từ Alfajores Faucet.

2. Triển khai Smart Contract

Truy cập Remix IDE: https://remix.ethereum.org/.

Tải file MicroSavings.sol lên.

Biên dịch (Compile) hợp đồng với phiên bản Solidity 0.8.0.

Trong tab Deploy & Run Transactions:

Chọn Environment: Injected Provider - MetaMask.

Đảm bảo đã kết nối với mạng Celo Alfajores.

Chọn Contract: MicroSavings.

Nhấp vào Deploy.

IV. Hướng Dẫn Tương Tác (Contract Interaction)

Sau khi triển khai thành công, bạn có thể tương tác với các chức năng cốt lõi:

Chức năng

Mô tả

approve()

BẮT BUỘC TRƯỚC KHI GỬI TIỀN. Phải gọi hàm này trên hợp đồng cUSD (0x874069Fa1c3883C669bEa471f2a3F8B3e791b4A5) để cấp quyền cho hợp đồng MicroSavings chi tiêu cUSD của bạn.

deposit(amount)

Gửi cUSD vào hợp đồng.

getAvailableBalance(user)

Kiểm tra tổng số tiền của người dùng (tiền gốc + lãi suất đã mô phỏng).

updateInterest()

Được gọi bởi Chủ sở hữu (Owner) để mô phỏng việc tính và tích lũy lãi suất.

withdrawAll()

Rút toàn bộ số dư hiện có (tiền gốc và lãi).

V. Các Bước Tiếp Theo

Phát triển giao diện người dùng (Frontend) bằng React hoặc Vue để tương tác với hợp đồng này.

Tích hợp với các giao thức DeFi (ví dụ: Moola Market) để tạo ra lợi nhuận thực tế thay vì lãi suất mô phỏng.

Thêm chức năng khóa tiền (Staking) để tăng cường tính ổn định
