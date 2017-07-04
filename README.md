# \<image-carousel\>

It's a carousel element for Polymer 2.0.

## Installation

  bower i image-carousel


## Example

    <image-carousel>
      <template slot="images" is="dom-repeat" items='["https://c2.staticflickr.com/2/1217/4607963354_e1a8fea210_z.jpg", "https://cs1.livemaster.ru/storage/e6/45/00b119c13ed9f8b4dc6363a60d--materialy-dlya-tvorchestva-nabor-dlya-vyshivki-biserom-belyj-ti.jpg", "https://tse4.mm.bing.net/th?id=ORT.TH_470633631&pid=1.12&eid=G.470633631"]'>
        <img class="scolling-images" src="[[item]]" width="100px" height="350px">
      </template>
    </image-carousel>


## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D


## License

MIT License