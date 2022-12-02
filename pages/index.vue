<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12" md="12">
        <h1 class="title-page">Chào mừng bạn quay trở lại</h1>
        <v-row>
          <v-col cols="6" sm="3">
            <v-card height="100%">
              <v-container fluid>
                <h3>Tổng số lượng người dùng</h3>
                <v-row height="100%">
                  <v-col>
                    <h4
                      class="grey--text text-h4 text-lg-h2 font-weight-bold lh-normal"
                    >
                      126
                    </h4>
                    <h5 class="font-weight-normal grey--text">+23% So với tháng trước</h5>
                  </v-col>
                  <v-col align-self="center" align="center">
                    <v-icon size="60" color="green"
                      >mdi-account-box-outline</v-icon
                    >
                  </v-col>
                </v-row>
              </v-container>
            </v-card>
          </v-col>
          <v-col cols="6" sm="3"
            ><v-card height="100%">
              <v-container fluid>
                <h3>Số lượng đơn hàng</h3>
                <v-row height="100%">
                  <v-col>
                    <h4
                      class="grey--text text-h4 text-lg-h2 font-weight-bold lh-normal"
                    >
                      70
                    </h4>
                    <h5 class="font-weight-normal grey--text">-3% So với tháng trước</h5>
                  </v-col>
                  <v-col align-self="center" align="center">
                    <v-icon size="60" color="warning">mdi-cart-plus</v-icon>
                  </v-col>
                </v-row>
              </v-container>
            </v-card></v-col
          >
          <v-col cols="6" sm="3"
            ><v-card height="100%">
              <v-container fluid>
                <h3>Số sản phẩm được bán</h3>
                <v-row height="100%">
                  <v-col>
                    <h4
                      class="grey--text text-h4 text-lg-h2 font-weight-bold lh-normal"
                    >
                      120
                    </h4>
                    <h5 class="font-weight-normal grey--text">-10% So với tháng trước</h5>
                  </v-col>
                  <v-col align-self="center" align="center">
                    <v-icon size="60" color="red">mdi-chart-areaspline</v-icon>
                  </v-col>
                </v-row>
              </v-container>
            </v-card></v-col
          >
          <v-col cols="6" sm="3"
            ><v-card height="100%">
              <v-container fluid>
                <h3>Views Summary</h3>
                <v-row height="100%">
                  <v-col>
                    <h4
                      class="grey--text text-h4 text-lg-h2 font-weight-bold lh-normal"
                    >
                      4124
                    </h4>

                    <h5 class="font-weight-normal grey--text">+50% Up</h5>
                  </v-col>
                  <v-col align-self="center" align="center">
                    <v-icon size="60" color="orange"
                      >mdi-remove-shopping-cart</v-icon
                    >
                  </v-col>
                </v-row>
              </v-container>
            </v-card></v-col
          >
        </v-row>
        <v-row>
          <v-col cols="12" lg="4">
            <v-card height="100%">
              <v-card-title>Bán theo danh mục</v-card-title>
              <v-card-text>
                <p>
                  Top 5 danh mục bán chạy nhất
                </p>
                <client-only placeholder="Loading...">
                  <DoughnutChart
                    :chart-data="doughChartData"
                    :chart-options="doughChartOptions"
                    :height="430"
                  />
                </client-only>
                <v-row>
                  <v-col cols="9">
                    Bên cạnh biều đồ thể hiện số lượng sản phẩm bán chạy theo danh mục, bạn còn có thể xuất file excel để chi tiết hơn tất cả sản phẩm</v-col
                  >
                  <v-col cols="3">
                    <v-btn type="submit" color="primary" small tile
                      >Xuất file</v-btn
                    ></v-col
                  ></v-row
                >
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" lg="8">
            <v-card height="100%" light>
              <v-card-title>Doanh thu theo từng danh mục</v-card-title>
              <v-card-text>
                <p>
                  Tổng doanh thu của một danh mục sẽ được tính bằng tổng giá trị sản phẩm bán ra của danh mục đó.
                </p>
                <!-- <v-col cols="3">
                      <v-select
                        :items="[
                          'Division 1',
                          'Division 2',
                          'Division 3',
                          'Division 4'
                        ]"
                        label="Division"
                        dense
                        outlined
                      ></v-select>
                    </v-col> -->
                <client-only placeholder="Loading...">
                  <LineChart
                    :chart-options="lineChartOptions"
                    :chart-data="lineChartData"
                    :chart-id="`chartId`"
                    :width="300"
                    :height="400"
                    :styles="{
                      margin: '1rem auto',
                      backgroundColor: 'rgba(255,255,255, .85)',
                      padding: '.75rem'
                    }"
                  />
                </client-only>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                  Voluptatum suscipit totam reiciendis molestiae dolorem facere
                  eaque, esse adipisci. Aperiam sapiente quod dolores, assumenda
                  voluptatum possimus nam fuga ducimus temporibus.
                </p>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="12" md="8">
            <v-card height="100%">
              <v-container fluid>
                <h3 class="title-page">
                  Lịch vạn niên
                </h3>
                <div>
                  Lịch đánh dấu thời điểm quan trọng
                </div>
                <v-calendar class="my-6"></v-calendar>
              </v-container>
            </v-card>
          </v-col>
          <v-col cols="12" md="4">
            <v-card height="100%">
              <v-container>
                <h3 class="title-page">Thông báo</h3>
                <div>
                  Ở đây sẽ có những thông báo mới nhất về đơn hàng của người dùng<br/>
                  O : Đơn hàng<br/>
                  P : Sản phẩm<br/>
                  C : Danh mục<br/>
                  U : Người dùng.
                </div>
                <v-container fluid>
                  <!-- <v-virtual-scroll width="256" height="321" item-height="120"> -->
                  <v-row no-gutters>
                    <v-col cols="2" align-self="center" align="center">
                      <v-avatar color="primary">
                        <span class="white--text font-weight-bold">O</span>
                      </v-avatar>
                    </v-col>
                    <v-col cols="10">
                      <blockquote class="blockquote grey--text body-1 px-3">
                        <div class="mb-1">
                          Đơn hàng #147 vừa được giao
                        </div>
                        <cite class="font-weight-thin"
                          >- Bạn có thể theo dõi đơn hàng trên HeyU</cite
                        >
                      </blockquote>
                    </v-col>
                  </v-row>
                  <v-row no-gutters>
                    <v-col cols="9">
                      <blockquote
                        class="blockquote grey--text body-1 px-3 text-right"
                      >
                        <div class="mb-1">
                          Trần Văn Phúc vừa đăng ký tài khoản
                        </div>
                        <cite class="font-weight-thin"
                          >- Xem thông tin mới nhất của người này</cite
                        >
                      </blockquote>
                    </v-col>
                    <v-col cols="3" align-self="center" align="center">
                      <v-avatar color="green">
                        <span class="white--text font-weight-bold">U</span>
                      </v-avatar>
                    </v-col>
                  </v-row>
                  <v-row no-gutters>
                    <v-col cols="2" align-self="center" align="center">
                      <v-avatar color="info">
                        <span class="white--text font-weight-bold">P</span>
                      </v-avatar>
                    </v-col>
                    <v-col cols="10">
                      <blockquote class="blockquote grey--text body-1 px-3">
                        <div class="mb-1">
                          Sản phẩm "Ủa? Genz" đã hết hàng trong kho
                        </div>
                        <cite class="font-weight-thin"
                          >- Hãy nhập thêm</cite
                        >
                      </blockquote>
                    </v-col>
                  </v-row>
                  <!-- <v-row no-gutters>
                      <v-col cols="9">
                        <blockquote
                          class="blockquote grey--text body-1 px-3 text-right"
                        >
                          <div class="mb-1">
                            Fugit nihil corporis rem iste! Doloremque inventore
                            natus nemo
                          </div>
                          <cite class="font-weight-thin"
                            >- Carol Violas. Sales Representative</cite
                          >
                        </blockquote>
                      </v-col>
                      <v-col cols="3" align-self="center" align="center">
                        <v-avatar color="green">
                          <span class="white--text font-weight-bold">CV</span>
                        </v-avatar>
                      </v-col>
                    </v-row>
                    <v-row no-gutters>
                      <v-col cols="2" align-self="center" align="center">
                        <v-avatar color="primary">
                          <span class="white--text font-weight-bold">AS</span>
                        </v-avatar>
                      </v-col>
                      <v-col cols="10">
                        <blockquote class="blockquote grey--text body-1 px-3">
                          <div class="mb-1">
                            Fugit nihil corporis rem iste! Doloribus magni
                            doloremque
                          </div>
                          <cite class="font-weight-thin"
                            >- Any Sanders. Sr Marketing Director</cite
                          >
                        </blockquote>
                      </v-col>
                    </v-row>
                    <v-row no-gutters>
                      <v-col cols="9">
                        <blockquote
                          class="blockquote grey--text body-1 px-3 text-right"
                        >
                          <div class="mb-1">
                            Fugit nihil corporis rem iste! Doloremque inventore
                            natus nemo
                          </div>
                          <cite class="font-weight-thin"
                            >- Carol Violas. Sales Representative</cite
                          >
                        </blockquote>
                      </v-col>
                      <v-col cols="3" align-self="center" align="center">
                        <v-avatar color="green">
                          <span class="white--text font-weight-bold">CV</span>
                        </v-avatar>
                      </v-col>
                    </v-row> -->
                  <!-- </v-virtual-scroll> -->
                </v-container>
              </v-container>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    <Footer />
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      doughChartData: {
        labels: ['Genz', 'Lịch sử', 'Văn học', 'Khoa học', 'Cổ tích'],
        datasets: [
          {
            label: 'Số lượng sản phẩm',
            data: [72, 131, 12, 3, 4],
            backgroundColor: [
              'rgba(20, 255, 0, 0.85)',
              'rgba(200, 5, 0, 0.85)',
              'rgba(10, 220, 0, 0.85)',
              'rgba(2, 100, 0, 0.85)',
              'rgba(20, 55, 0, 0.85)',
            ],
            borderColor: 'rgba(100, 155, 0, 1)',
            borderWidth: 0
          }
        ]
      },
      doughChartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        offset: 8,
        radius: 160,
        spacing: 4,
        hoverOffset: 32,
        hoverBorderWidth: 1,
        weight: 0
      },
      lineChartData: {
        labels: [
          'Jan',
          'Feb',
          'Mar',
          'Apr',
          'May',
          'Jun',
          'Jul',
          'Aug',
          'Sep',
          'Oct',
          'Nov',
          'Dec'
        ],
        datasets: [
          {
            label: 'John Doe',
            backgroundColor: '#ff0099',
            borderColor: '#ff0099',
            borderWidth: '0',
            borderJoinStyle: 'round',
            data: [40, 39, 10, 40, 39, 80, 40, 30, 10, 20, 30, 40]
          },
          {
            label: 'Jane Doe',
            backgroundColor: '#ff9900',
            borderColor: '#ff9900',
            borderWidth: '0',
            borderJoinStyle: 'round',
            data: [20, 9, 80, 90, 29, 58, 80, 20, 30, 40, 55, 75]
          },
          {
            label: 'Jack Doe',
            backgroundColor: '#999999',
            borderColor: '#999999',
            borderWidth: '0',
            borderJoinStyle: 'round',
            data: [10, 24, 42, 50, 69, 10, 20, 70, 89, 45, 35, 42]
          }
        ]
      },
      lineChartOptions: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  },
  head() {
    return {
      title: 'Homepage - Nuxtify Admin Dashboard Template by dykraf.com',
      description:
        'A Collection of Templates in Nuxtify Admin Template Dashboard by dykraf.com'
    }
  }
}
</script>
