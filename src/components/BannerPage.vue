<template>
  <div class="container">
    <div class="row">
      <div class="col-6 middle-hori">
        <h3 class="matcha-color kindly-font">
          Hello! <span style="font-size: 15px">My name is</span>
        </h3>

        <div class="typewriter">
          <h1>Wannaporn Temsiritrakul</h1>
        </div>

        <p>
          I'm a junior software engineer who genuinely passionate about software
          engineering and coding. I have keen interest in Software Architecture
          and also enjoy web developing. I'm seeking out new challenges and
          willing to learn new things.
        </p>
        <div class="ta-center" id="#resume">
          <a type="button" class="btn matcha-button" @click="downloadItem()">Resume</a>
          <!-- <a
            @click="downloadItem()"
          >download</a> -->
        </div>
      </div>
      <div class="col-6 margin-auto">
        <img :src="image" class="img-size just-right" />
      </div>
    </div>
  </div>
</template>
<script>
import nan_story from "../assets/nanaja_story.jpg";
import resume from "../assets/wannaporn_temsiritrakul_resume.jpg";
import axios from "axios";
export default {
  name: "BannerPage",
  data() {
    return {
      image: nan_story,
    };
  },
  methods: {
    downloadItem() {
      // el: '#resume',
      axios({
        url: resume,
        method:'GET',
        responseType:'blob'
      }).then((response)=>{
        var fileUrl = window.URL.createObjectURL(new Blob([response.data]))
        var fileLink = document.createElement('a')
        fileLink.href = fileUrl

        fileLink.setAttribute('download', resume)
        document.body.appendChild(fileLink)

        fileLink.click()
      })

    },
  },
};
</script>

<style>
h1 {
  color: #c79a96;
  font-weight: 800;
}

.img-size {
  width: 90%;
  height: auto;
}
.just-right {
  float: right;
}

/* .test-font-size{
    front-size: 180%
} */
.typewriter h1 {
  border-right: 0.15em solid orange;
  overflow: hidden;
  animation-fill-mode: forwards;
  white-space: nowrap;

  margin: 0;
  letter-spacing: 0.1em;
  animation: typewriter 5s steps(23) infinite alternate,
    blinking-cursor 0.5s steps(23) infinite normal;
}
@keyframes typewriter {
  0% {
    width: 0;
  }
  50% {
    width: 95%;
  }
  100% {
    width: 0%;
  }
}
@keyframes blinking-cursor {
  from,
  to {
    border-color: #c79a96;
  }
  50% {
    border-color: transparent;
  }
}

@media only screen and (max-width: 1200px) {
  h1 {
    font-size: 30px;
  }
  @keyframes typewriter {
    0% {
      width: 0;
    }
    50% {
      width: 85%;
    }
    100% {
      width: 0%;
    }
  }
}
@media only screen and (max-width: 975px) {
  h1 {
    font-size: 20px;
  }
  h3 {
    font-size: 18px;
  }
  @keyframes typewriter {
    0% {
      width: 0;
    }
    50% {
      width: 77%;
    }
    100% {
      width: 0%;
    }
  }
}

@media only screen and (max-width: 760px) {
  h1 {
    font-size: 16px;
  }
  h3 {
    font-size: 15px;
  }
  @keyframes typewriter {
    0% {
      width: 0;
    }
    50% {
      width: 90%;
    }
    100% {
      width: 0%;
    }
  }
}

@media only screen and (max-width: 500px) {
  h1 {
    font-size: 16px;
  }
  @keyframes typewriter {
    0% {
      width: 0;
    }
    50% {
      width: 100%;
    }
    100% {
      width: 0%;
    }
  }
}
</style>
