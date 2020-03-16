<template>
  <div class="footer">
    <div class="container">
      <img src="../assets/img/big-logo.png" alt="shockworks">
      <div class="footer-container">
        <div class="footer-part">
          <h4>Contact Us</h4>
          <ul class="footer-list">
            <li class="footer-icons"><i class="fas fa-phone-alt"></i><a href="tel:+18245428" class="footer-link">+(1) 824-5428</a></li>
            <li class="footer-icons"><i class="fas fa-map-marker"></i><a href="#" class="footer-link">Miami, United States</a></li>
            <li class="footer-icons"><img src="../assets/img/envelope.png" alt="email" class="footerimg-icon"><a href="mailto:yfuentes@shokworks.io" class="footer-link">yfuentes@shokworks.io</a></li>
          </ul>
        </div>
        <div class="footer-part">
          <h4>Our Company</h4>
          <ul class="footer-list">
            <li><a href="#">About</a></li>
            <li><a href="#">Product</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Career</a></li>
            <li><a href="#">Blog</a></li>
          </ul>

        </div>
        <div class="footer-part">
          <h4>Social Contacts</h4>
          <ul class="footer-list">
            <li><a href="#">Facebook</a></li>
            <li><a href="#">Linked In</a></li>
            <li><a href="#">Youtube</a></li>
            <li><a href="#">Vimeo</a></li>
            <li><a href="#">Skype</a></li>
          </ul>

        </div>
        <div class="footer-part">
          <h4>Address</h4>
          <p>Internet Systems Consortium, Inc. 950 Charter Street Redwood City, CA USA.</p>
          <h4>Follow Us</h4>
          <ul class="footer-rrss">
            <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
            <li><a href="#" class="skype"><i class="fab fa-skype"></i></a></li>
            <li><a href="#" class="linkedin"><i class="fab fa-linkedin-in"></i></a></li>
            <li><a href="#" class="instagram"><i class="fab fa-instagram"></i></a></li>
          </ul>
        </div>
      </div>

    </div>
  </div>
</template>

<style lang="scss">
.footer{
  text-align: center;
  background-image: url('../assets/img/footer-back.png');
  background-size: 100%;
  background-position: bottom left;
  background-repeat: no-repeat;
  padding-bottom: 320px;

  @media (max-width: 920px) {
    padding-bottom: 100px;
  }

  img {
    width: 100%;
    max-width: 525px;
    margin-bottom: 50px;
  }
  .footer-container {
    display: flex;
    align-items: flex-start;
    justify-content: space-around;

    @media (max-width: 920px) {
      flex-direction: column;
    }

    .footer-part {
      width: 25%;
      text-align: left;
      font-family: poppins;

      @media (max-width: 920px) {
        width: 100%;
      }

      h4 {
        margin-bottom: 15px;
      }

      p {
        margin: 20px 0 20px;
      }

      .footer-list {
        list-style: none;
        padding: 0;
        color: #777777;

        li {
          font-size: 15px;
          line-height: 2.5;
          display: flex;
          align-items: center;
          justify-content: flex-start;

          &.footer-icons {
            margin-bottom: 25px;
          }

          img {
            max-width: 29px;
            margin: 0 10px 0 0;
          }

          i {
            font-size: 27px;
            color: #9d60eb;
            margin: 0 10px 0 0;
          }

          a {
            color: inherit;
            text-decoration: none;
          }
        }
      }

      .footer-rrss {
        list-style: none;
        padding: 0;
        display: flex;
        margin-top: 30px;

        li {
          transition: all ease 0.3s;

          &:hover {
            transform: translate(0px, -5px);
          }

          a {
            background: rgb(99,98,215);
            background: linear-gradient(0deg, rgba(99,98,215,1) 0%, rgba(255,143,226,1) 100%);
            padding: 13px 24px;
            border-radius: 50px;
            position: relative;
            margin-right: 20px;
            color: #fff;

            &.skype {
              background: rgb(0,181,108);
              background: linear-gradient(25deg, rgba(0,181,108,1) 0%, rgba(158,230,157,1) 100%);
            }

            &.linkedin {
              background: rgb(255,154,182);
              background: linear-gradient(25deg, rgba(255,154,182,1) 0%, rgba(240,50,149,1) 100%);
            }

            &.instagram {
              background: rgb(240,147,118);
              background: linear-gradient(25deg, rgba(240,147,118,1) 0%, rgba(240,219,121,1) 100%);
            }

            i {
              position: absolute;
              top: 16px;
              left: 16px;
              margin: 0;
              font-size: 20px;

            }
          }
        }

      }
    }
  }
}
</style>