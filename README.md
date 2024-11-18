# Sokeio Example


```
<script sokeio-application-template type="javascript/x-template">
        const template={
          state: {
            count: 0,
          },
          updateTime() {
            setTimeout(() => {
              this.count = new Date();
              this.updateTime();
            }, 1000); 
          },
          ready() {
            this.updateTime();
          },
          render() {
            return `<div>
                <h1>hello world</h1>
                <p so-text="count">dfdfdfdf</p>
                <button class="btn btn-primary" so-on:click="count++;">click</button>
            </div>`;
          }
        };
        export default {
          components: {
            'sokeio::template': template
          },
          state: {
            count: 0,
          },
          updateTime() {
            setTimeout(() => {
              this.count = new Date();
              this.updateTime();
            }, 1000);
          },
          ready() {
            this.updateTime();
          },
          render() {
            return `<div>
                <h1>hello world</h1>
                <p so-text="count">dfdfdfdf</p>
                <button class="btn btn-primary" so-on:click="count++;">click</button>
                <button class="btn btn-primary" so-on:click="refresh();">Refresh</button>
                [sokeio::template/]
            </div>`;
          },
        };
      </script>
```
