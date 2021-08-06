<template>
  <div class="container">
    <div class="advertise">
      <h2 class="advertise-text">Giảm giá khi mua 2 sản phẩm trở lên</h2>
      <ul class="menu">
        <li class="menu-item">
          <a href="" class="menu-link">Giới thiệu</a>
        </li>
        <li class="menu-item">
          <a href="" class="menu-link">Báo giá</a>
        </li>
        <li class="menu-item">
          <a href="" class="menu-link">Hỏi đáp</a>
        </li>
        <li class="menu-item">
          <a href="" class="menu-link">Hướng dẫn</a>
        </li>
        <li class="menu-item">
          <a href="" class="menu-link">Liên hệ</a>
        </li>
      </ul>
    </div>
    <div class="header">
      <div class="logo">
        <img class="logo-image" src="../assets/logo.png" alt="Du Khanh logo" />
      </div>

      <div class="search-box">
        <input type="text" placeholder="Nhập để tìm kiếm" />
        <button class="button" type="submit">Tìm kiếm</button>
      </div>
      <div class="hotline">
        <i class="fas fa-phone-alt"></i>
        <p>Số điện thoại</p>
        <p>097.279.0435<br />0912.544.146</p>
      </div>
    </div>
    <div class="category-part">
      <ul class="category">
        <li class="category-item">
          <a href="" class="category-link">Trang chủ</a>
        </li>
        <li class="category-item">
          <a href="" class="category-link">Phòng khách</a>
        </li>
        <li class="category-item">
          <a href="" class="category-link">Phòng ngủ</a>
        </li>
        <li class="category-item">
          <a href="" class="category-link">Phòng bếp</a>
        </li>
      </ul>
    </div>
    <div class="intro">
      <div class="slider">
        <div class="myslider fade">
          <div class="txt">
            <h1>Đồ gỗ mỹ nghệ Du Khánh</h1>
            <p>
              Tất cả vì khách hàng<br />Chuyên nhận hàng đặt, sản xuất các loại
              giường, tủ, bàn ghế
            </p>
          </div>
          <div
            class="panel"
            style="
              background-image: url('../assets/sofa-go-oc-cho-hien-dai-noi-that-lac-gia-3-1920x640.jpg');
            "
          ></div>
        </div>

        <a class="prev" onclick="plusSlides(-1)"
          ><i class="fas fa-chevron-circle-left"></i
        ></a>
        <a class="next" onclick="plusSlides(1)"
          ><i class="fas fa-chevron-circle-right"></i
        ></a>

        <div class="dotsbox" style="text-align: center">
          <span class="dot" onclick="currentSlide(1) "></span>
          <span class="dot" onclick="currentSlide(2) "></span>
          <span class="dot" onclick="currentSlide(3) "></span>
          <span class="dot" onclick="currentSlide(4) "></span>
          <span class="dot" onclick="currentSlide(5) "></span>
        </div>
      </div>
    </div>

    <div class="main">
      <div class="new-product">
        <div class="caption">
          <div class="tab-caption tab-selected">
            <div class="head-title head-selected">Sản phẩm khuyến mại</div>
          </div>
          <div class="tab-caption">
            <div class="head-title">Sản phẩm mới</div>
          </div>
        </div>
        <div class="list">
          <!-- custom elements in iteration require v-bind:key directives -->
          <ProductCard
            v-for="product in products"
            :key="product.id"
            :product="product"
          />
        </div>
      </div>
      <!-- <div class="product-category">
        <div class="caption">
          <div class="head-title">Phòng khách</div>
          <div class="sub-category">
            <ul class="list-sub-category">
              <li class="sub-category-item">
                <a href="" class="sub-category-link active-sub">Bàn nước</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Kệ ti vi</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Tủ trang trí phòng</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Tủ giày</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="list">
          <div class="list-item">
            <img src="../assets/28-1.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
        </div>
      </div>
      <div class="product-category">
        <div class="caption">
          <div class="head-title">Phòng bếp</div>
          <div class="sub-category">
            <ul class="list-sub-category">
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Bàn nước</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Kệ ti vi</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Tủ trang trí phòng</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Tủ giày</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="list">
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
        </div>
      </div>
      <div class="product-category">
        <div class="caption">
          <div class="head-title">Phòng ngủ</div>
          <div class="sub-category">
            <ul class="list-sub-category">
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Bàn nước</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Kệ ti vi</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Tủ trang trí phòng</a>
              </li>
              <li class="sub-category-item">
                <a href="" class="sub-category-link">Tủ giày</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="list">
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-item">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
        </div>
      </div>
      <div class="evaluate">
        <div class="caption">
          <div class="head-title">Đánh giá của khách hàng</div>
        </div>
        <div class="list">
          <div class="list-evaluate">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-evaluate">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
          <div class="list-evaluate">
            <img src="../assets/item.jpg" alt="" class="list-image" />
            <div class="list-title">Như ý voi gỗ hương</div>
            <div class="list-desc">
              <p class="sale-price">60.000.000 VNĐ</p>
              <p class="price">55.000.000 VNĐ</p>
            </div>
          </div>
        </div>
      </div> -->
    </div>

    <div class="footer">
      <div class="evaluate-container">
        <div class="customer-evaluate">
          <form action="" method="get">
            <div class="quality form-row">
              <div for="quality">Chất lượng sản phẩm</div>
              <div>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
              </div>
            </div>
            <div class="name form-row">
              <div for="name">Tên khách hàng</div>
              <input type="text" placeholder="Nhập tên" />
            </div>
            <div class="address form-row">
              <div for="address">Địa chỉ</div>
              <input type="text" placeholder="Nhập địa chỉ" />
            </div>
            <div class="boughtproduct form-row">
              <div for="boughtproduct">Sản phẩm đã mua</div>
              <select name="product" id="">
                <option value="">Ghế</option>
                <option value="">Giường</option>
              </select>
            </div>
            <div class="comment form-row">
              <div for="comment">Đánh giá</div>
              <br />
              <textarea name="" id="" cols="30" rows="10"></textarea>
            </div>
          </form>
        </div>
      </div>
      <div class="infor">
        <div class="infor-column">
          <div class="head-title">Cơ sở sản xuất đồ gỗ mỹ nghệ Du Khánh</div>
          <div class="infor-desc">
            <p>Địa chỉ: Cổ Châu - Vân Hà - Đông Anh - Hà Nội</p>
            <p>
              Giấy phép kinh doanh số.. do phòng Kinh doanh sở ... Thành phố Hà
              Nội cấp ngày...
            </p>
            <p>Nhà máy sản xuất:</p>
            <p>Mở cửa 7h30 - 20h tất cả các ngày trong tuần</p>
          </div>
        </div>
        <div class="infor-column">
          <div class="head-title">Liên hệ & Thanh toán</div>
          <div class="infor-desc">
            <p>Chủ xưởng: Lê Văn Du</p>
            <p>Số điện thoại: 0379700427 hoặc 0912544146</p>
            <p>Website: www....</p>
          </div>
        </div>
        <div class="infor-column">
          <div class="head-title">Hỗ trợ khách hàng</div>
          <div class="infor-desc">
            <p>Chính sách bảo mật thông tin</p>
            <p>Chính sách và quy định</p>
            <p>Sơ đồ chỉ đường</p>
            <p>
              Đăng ký nhận thông tin khuyến mãi qua số điện thoại hoặc email
            </p>
            <input type="text" placeholder="Nhập số điện thoại hoặc email" />
            <button type="submit" class="button">Đăng ký</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductCard from "@/components/ProductCard.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    ProductCard,
  },
  data() {
    return {
      products: null,
    };
  },
  created() {
    axios
      .get(
        "localhost:8888/api/v1/product/get-list-product-by-subcategory?subcategoryId=5&parentCategoryId=1"
      )
      .then((response) => console.log("products", response.data))
      .catch((error) => console.log(error));
  },
};
</script>
