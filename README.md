![license-badge]

  <h1 align="center">E-Commerce Back End</h1>
  
  <!-- TABLE OF CONTENTS -->
  <details>
    <summary>Table of Contents</summary>
    <ul>
      <li><a href="#description">Description</a></li>
      <li><a href="#installation">Installation</a></li>
      <li><a href="#usage">Usage</a></li>
      <li><a href="#contributing">Contributing</a></li>
      <li><a href="#license">License</a></li>
      <li><a href="#questions">Questions</a></li>
    </ul>
  </details>

  </br>
  
  ## Description
  E-Commerce Back End is a Node.js application, which uses Sequelize as the ORM. It includes API endpoints that allow the user to interact with the e-commerce database and implement CRUD methods.
  
  ## Installation
1. First, ensure you have node.js and MySQL installed
2. Clone the repository to your local machine
3. Run the command `npm install`
4. Start MySQL through the command line in the root folder and run `source db/schema.sql` to create the Ecommerce database.
5. Run `npm run seed` to seed the database
6. Run `npm start` to start the server.
7. View the endpoints in the folder routes/api/index/ to see all the possible endpoints.
8. Endpoints can be tested using Insomnia referring to the code comments for help with sending data in the body for POST and PUT routes. 
## Usage

This application can be used as a starting point for an ecommerce site. It uses Sequelize models to separate product data into separate tables for keeping accurate records.

## Contributing

1. Fork the repository
2. Create your Feature Branch (git checkout -b feature/`yourfeature`)
3. Commit your Changes (git commit -m 'Add some feature')
4. Push to the Branch (git push origin feature/`yourfeature`)
5. Open a pull request with a comment describing your changes.

## License

Licensed under the MIT License.

## Questions

Email: [mannysg88@gmail.com](mailto:mannysg88@gmail.com)

Github: [https://github.com/Mannygarcia98](https://github.com/Mannygarcia98)

  <!-- MARKDOWN LINKS & IMAGES -->

[license-badge]: https://img.shields.io/badge/LICENSE-MIT-brightgreen?style=plastic
