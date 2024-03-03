## Project Overview

The task involves developing a web application that allows users to browse through a list of stores categorized by various parameters. Users should be able to filter, sort, and search for stores based on different criteria. Additionally, they should have the ability to bookmark their favorite stores, with these preferences stored locally and reflected in the UI.

## Github Repo:
https://github.com/enacton-tech/react-intermediate

### Video Explanation
https://app.usebubbles.com/iHAEumYaUzLzDQzhTkrWw9/untitled

### Setting Up the Project

To set up the project locally, follow these steps:

1. Clone the repository and navigate to the project folder.
2. Run `npm install`.
3. Start the project using `npm run start`.
4. Access the React website at http://localhost:3000 and the API at http://localhost:3001.

### API Consumption

#### Store List API:
- **Get List of Stores**: Retrieve a list of stores. 
   Example: http://localhost:3001/stores

#### Category List API:
- **Get List of Categories**: Retrieve a list of categories. 
   Example: http://localhost:3001/categories

#### Store Filter:
- **cats**: Filter stores by category. 
   Example: http://localhost:3001/stores?cats=1

- **cashback_enabled**: Filter stores with cashback enabled. 
   Example: http://localhost:3001/stores?cashback_enabled=1

- **is_promoted**: Filter stores that are promoted. 
   Example: http://localhost:3001/stores?is_promoted=1

- **is_sharable**: Filter stores that allow sharing. 
   Example: http://localhost:3001/stores?is_sharable=1

- **status**: Filter stores by status (publish|draft|trash). 
   Example: http://localhost:3001/stores?status=draft

- **alphabet**: Filter stores by starting alphabet character. 
   Example: http://localhost:3001/stores?name_like=^a

- **multiple filters**: Filter stores using multiple criteria. 
   Example: http://localhost:3001/stores?name_like=^a&cashback_enabled=1&status=publish

#### Search:
- **store search by name**: Search stores by name. 
   Example: http://localhost:3001/stores?name_like=ali

#### Store Sort:
- **name**: Sort stores by name. 
   Example: http://localhost:3001/stores?_sort=name

- **featured**: Sort stores by featured status in descending order. 
   Example: http://localhost:3001/stores?_sort=featured&order=desc

- **popularity**: Sort stores by popularity based on clicks in descending order. 
   Example: http://localhost:3001/stores?_sort=clicks&_order=desc

- **cashback**: Sort stores by cashback amount. 
   Example: http://localhost:3001/stores?_sort=amount_type,cashback_amount&_order=asc,desc

#### Pagination:
- Paginate the results with page number and limit parameters. 
   Example: http://localhost:3001/stores?_page=1&_limit=20

For more information, refer to the [JSON Server Documentation](https://github.com/typicode/json-server/tree/v0?tab=readme-ov-file).

### Requirements

1. **Project Setup**: Ensure the project is set up correctly according to the provided instructions.

2. **Sidebar Categories**: Display a list of available categories in the sidebar.

3. **Main Section**: Show a paginated list of stores in the main section, loading only the first page initially.

4. **Infinite Scroll**: Implement infinite scroll to load more stores dynamically as the user scrolls, similar to Instagram feeds.

5. **Category Filter**: Filter stores based on the selected category and highlight the selected category in the sidebar.

6. **Store Sorting**: Provide options to sort stores by name, featured, popularity, and cashback.

7. **Store Filters**: Allow filtering by category, status (active, coming soon, discontinued), alphabet, and boolean attributes such as cashback enabled, promoted, and share & earn enabled.

8. **Store Search**: Enable searching stores by name.

9. **Bookmark Stores**: Allow users to favorite stores, with the favorite status stored locally and indicated by a red heart icon in the UI.

10. **URL Parameters**: Store filter, search, and sort options in the URL parameters to replicate the user's browsing state when sharing URLs.

### Store Card Rendering

- **Store Logo and Name**: Render the store card with the store logo centered followed by its name.

- **Cashback Display Logic**:
  - If `cashback_enabled` is `0`, display "No cashback available".
  - If `cashback_enabled` is `1`, construct the cashback string as follows:
    - Start with the `rate_type` attribute, which can be either "upto" or "flat".
    - Check the `amount_type`:
      - If it is "fixed", prefix the `cashback_amount` with "$".
      - If it is "percent", suffix the `cashback_amount` with "%".
    - Ensure the `cashback_amount` is formatted to two decimal places.

- **Favourite Button**: Include a favourite button in the top right corner of the store card. Clicking this button should mark the store as a favourite.

- **Store Card Interaction**: Clicking on the store card should redirect the user to the store's home page.
- **Example**: "Upto $10.00 cashback" or "Flat 5.00% cashback".

### Links

1. **Reference Page All Stores**: [Stores with Category Filter](https://laraback.enactweb.com/all-stores)
2. **Reference Page**: [Infinite Scroll Stores Page](https://stg-app.rewardsbunny.com/all-stores)
3. **Recording Video**: [Record with Bubbles](https://app.usebubbles.com/)
4. **JSON Server Documentation**: [JSON Server API Documentation](https://github.com/typicode/json-server/tree/v0?tab=readme-ov-file)

### Required Screens

- Store Page: ![Store Page](https://img.enacton.com/ShareX/2024/03/mdRHpBKvGa.png)

### Delivery Expectations

1. **Code Repository**: Push the code to a public GitHub repository.

2. **Documentation**: Provide well-documented code with a comprehensive README file.

3. **Setup Instructions**: Include clear instructions on how to set up and run the project.

4. **Application Demo**: Record a video demonstrating the application's functionality.

### Evaluation Criteria

Candidates will be evaluated based on the following criteria:

1. **Functionality**: Does the application meet all specified requirements?
2. **Code Quality**: Is the code well-structured, readable, and maintainable?
3. **Documentation**: Is the codebase well-documented with clear instructions?
4. **User Experience**: Does the application provide a smooth and intuitive user experience?
5. **Technical Proficiency**: How effectively does the candidate utilize relevant technologies and APIs?
6. **Delivery Quality**: Does the candidate deliver all expected deliverables with high quality?

## Conclusion

We're thrilled to witness your skills in action as you tackle this project. Your dedication and creativity will play a vital role in crafting a seamless user experience. Best of luck, and we're excited to see your contributions!