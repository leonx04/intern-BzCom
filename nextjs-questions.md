Dưới đây là một số câu hỏi cơ bản về Next.js mà bạn có thể gặp trong phỏng vấn frontend:

1. **Next.js là gì?**
   - Next.js là một framework React cho phép xây dựng các ứng dụng web với khả năng render phía server (SSR), tạo trang tĩnh (SSG), và hỗ trợ khả năng routing, tối ưu hóa hiệu suất và nhiều tính năng mạnh mẽ khác.

2. **Sự khác biệt giữa Static Generation (SSG) và Server-side Rendering (SSR) trong Next.js là gì?**
   - **SSG (Static Site Generation)**: Tạo các trang web tĩnh tại thời điểm build và phục vụ chúng cho người dùng. Sử dụng `getStaticProps` và `getStaticPaths`.
   - **SSR (Server-side Rendering)**: Render trang mỗi khi có yêu cầu từ người dùng, giúp lấy dữ liệu mới nhất mỗi lần truy cập. Sử dụng `getServerSideProps`.

3. **Next.js sử dụng hệ thống routing như thế nào?**
   - Next.js sử dụng routing dựa trên cấu trúc thư mục. Mỗi file trong thư mục `pages` sẽ tự động trở thành một route trên ứng dụng. Ví dụ: `pages/index.js` sẽ trở thành route `/`, và `pages/about.js` sẽ là route `/about`.

4. **Cách tạo một API Route trong Next.js là gì?**
   - Bạn có thể tạo API route trong thư mục `pages/api`. Mỗi file trong thư mục này sẽ trở thành một endpoint API. Ví dụ: `pages/api/hello.js` có thể chứa một API đơn giản:
     ```js
     export default function handler(req, res) {
       res.status(200).json({ message: 'Hello, world!' });
     }
     ```

5. **`getStaticProps` và `getServerSideProps` khác nhau như thế nào?**
   - **`getStaticProps`**: Được sử dụng để lấy dữ liệu và render trang ở thời điểm build (SSG). Trang sẽ được tạo sẵn khi build và được phục vụ nhanh chóng cho người dùng.
   - **`getServerSideProps`**: Được sử dụng để lấy dữ liệu và render trang mỗi lần có yêu cầu từ người dùng (SSR). Thường được dùng khi cần dữ liệu động, luôn cập nhật.

6. **Sự khác biệt giữa `getStaticPaths` và `getStaticProps` là gì?**
   - **`getStaticPaths`**: Dùng để chỉ định các paths động cần được tạo trước khi build, thường được sử dụng cùng với `getStaticProps` để tạo các trang tĩnh động.
   - **`getStaticProps`**: Lấy dữ liệu cho các trang tĩnh, giúp trang được render trước khi gửi đến người dùng.

7. **Next.js có hỗ trợ HMR (Hot Module Replacement) không?**
   - Có, Next.js hỗ trợ HMR mặc định trong chế độ phát triển (development mode). Điều này giúp tự động cập nhật trang khi bạn thay đổi mã nguồn mà không cần tải lại trang.

8. **Chức năng Image Optimization trong Next.js là gì?**
   - Next.js cung cấp một component `<Image>` tối ưu hóa hình ảnh tự động, giúp giảm kích thước hình ảnh và tải chúng nhanh hơn. Hình ảnh được tự động điều chỉnh kích thước, nén, và định dạng tùy thuộc vào thiết bị người dùng.

9. **Next.js hỗ trợ CSS như thế nào?**
   - Next.js hỗ trợ CSS qua các phương thức như:
     - **Global CSS**: Thêm CSS toàn cục trong tệp `pages/_app.js`.
     - **CSS Modules**: Cung cấp CSS chỉ áp dụng cho từng component cụ thể.
     - **Styled-components** và các thư viện CSS-in-JS khác.

10. **Next.js có hỗ trợ TypeScript không?**
    - Có, Next.js hỗ trợ TypeScript ngay từ đầu. Bạn chỉ cần tạo các tệp `.ts` hoặc `.tsx` trong dự án và Next.js sẽ tự động thiết lập cấu hình TypeScript.

11. **Cách cấu hình môi trường (Environment Variables) trong Next.js là gì?**
    - Bạn có thể sử dụng các biến môi trường trong Next.js bằng cách tạo các tệp `.env.local`, `.env.production`, `.env.development`. Các biến này sẽ được truy cập thông qua `process.env.VARIABLE_NAME`.

12. **Cách sử dụng Layouts trong Next.js?**
    - Next.js hỗ trợ layouts thông qua việc tạo các component bao bọc các trang. Ví dụ, bạn có thể tạo một `Layout` component và sử dụng nó trong các trang của bạn để có một cấu trúc chung (ví dụ: header, footer).

13. **Cách tối ưu hóa hiệu suất trong Next.js?**
    - Next.js cung cấp nhiều tính năng để tối ưu hóa hiệu suất:
      - **Automatic Static Optimization**: Nếu trang không yêu cầu dữ liệu từ server, Next.js sẽ tự động render trang tĩnh.
      - **Image Optimization**: Dùng component `<Image>` để tối ưu hóa tải hình ảnh.
      - **Code Splitting**: Tự động tách mã JavaScript thành các phần nhỏ để tải nhanh hơn.

14. **Cách cấu hình `404` và `500` page trong Next.js là gì?**
    - Bạn có thể tạo các trang lỗi bằng cách tạo tệp `pages/404.js` và `pages/500.js` để tùy chỉnh nội dung hiển thị khi người dùng truy cập vào trang không tồn tại hoặc gặp lỗi máy chủ.

15. **Next.js hỗ trợ các tính năng SEO như thế nào?**
    - Next.js hỗ trợ SEO thông qua:
      - **Dynamic Rendering**: Dùng SSR và SSG để tạo các trang động với nội dung SEO-friendly.
      - **Head Component**: Sử dụng component `<Head>` để thêm các thẻ meta, title, và link cho SEO.

16. **Cách sử dụng Custom Server trong Next.js là gì?**
    - Bạn có thể sử dụng custom server trong Next.js để kiểm soát cách ứng dụng được phục vụ. Ví dụ, bạn có thể dùng Express.js hoặc Koa.js làm server thay thế mặc định của Next.js.

17. **Cách tạo một Progressive Web App (PWA) trong Next.js?**
    - Next.js có thể dễ dàng biến thành PWA bằng cách sử dụng các thư viện như `next-pwa`. Bạn cần cấu hình service worker và cache để đảm bảo trang có thể hoạt động offline và tải nhanh.

18. **Cách xử lý lỗi trong Next.js?**
    - Bạn có thể xử lý lỗi trong Next.js bằng cách sử dụng các page như `pages/_error.js` để tùy chỉnh thông báo lỗi khi có lỗi xảy ra. Ngoài ra, Next.js còn hỗ trợ các lỗi khi sử dụng SSR hoặc SSG.

Các câu hỏi này giúp phỏng vấn viên đánh giá khả năng của bạn trong việc hiểu và làm việc với Next.js, khả năng sử dụng các tính năng mạnh mẽ của Next.js để xây dựng ứng dụng web nhanh chóng và hiệu quả.
