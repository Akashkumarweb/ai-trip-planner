# Easy Trip AI

**Live Demo:** [https://easytripai.com/](https://easytripai.com/)

Easy Trip AI is a full-stack, AI-powered travel planner that helps users design the perfect trip itinerary, discover cultural insights, and organize packing lists—all from one intuitive interface.

> **Note:** The source code for this project is kept in a **private GitHub repository** to protect intellectual property and sensitive API keys. The following information provides a detailed overview of the project’s features, technology stack, challenges, and outcomes without exposing the underlying source code.

---

## 1. Project Overview & Purpose

### **Motivation**
- **Seamless Trip Planning:** Existing travel apps often require juggling multiple resources to plan a trip. Easy Trip AI aims to centralize itinerary creation, cultural insight discovery, and packing list generation.
- **AI-Driven Personalization:** By incorporating user preferences and personality traits, the app offers recommendations tailored to each traveler’s pace, budget, and interests.

### **Goals**
1. Provide a **user-friendly interface** for generating custom travel itineraries.
2. Integrate **AI-based suggestions** for hidden gems, local insights, and cultural etiquette.
3. Offer **intuitive drag-and-drop** capabilities for itinerary rearrangement.
4. Deliver **smart packing lists** to save time and reduce the stress of preparing for trips.

---

## 2. Technologies & Tools Used

- **Next.js 15**  
  For server-side rendering, API routes, and the React-based structure of the app.
- **React 19**  
  Client-side components, dynamic UI updates, and state management.
- **Tailwind CSS**  
  Rapid UI styling and responsive design.
- **DND Kit** (`@dnd-kit/core`, `@dnd-kit/sortable`)  
  Drag-and-drop interactions in the Itinerary Editor.
- **MapLibre GL**  
  Interactive maps for visualizing trip locations and hidden gems.
- **OpenAI GPT-4**  
  Provides AI suggestions for itineraries, cultural tips, and packing lists.
- **Lucide React**  
  Icon set used throughout the app (e.g., for navigation, buttons, etc.).
- **Node.js**  
  Environment for server-side code (API routes) and dependency management.
- **PM2** (Optional)  
  Process manager for keeping the Node.js app running persistently on a server.

---

## 3. Key Features

1. **AI-Powered Itinerary Generation**  
   - Users provide a destination and preferences.  
   - The system queries OpenAI GPT-4 to create a multi-day plan, complete with hidden gems and coordinates.

2. **Travel Personality Quiz**  
   - Collects user pace, interests, and budget.  
   - Customizes itinerary recommendations accordingly.

3. **Drag-and-Drop Itinerary Editor**  
   - Built with DND Kit.  
   - Users can reorder days and activities for a custom plan.

4. **Cultural Insights & Etiquette**  
   - AI-powered tips for local customs and norms.  
   - Helps users avoid faux pas and immerse themselves in local culture.

5. **Smart Packing List**  
   - Dynamically generated items based on itinerary activities, climate, and cultural considerations.

6. **Interactive Map**  
   - MapLibre GL integration for location visualization.  
   - Marks hidden gems and highlights to give travelers a geographical overview.

---

## 4. Screenshots & GIFs

> **Note:** Sample images are shown below to demonstrate the interface. They do **not** reveal code.

   <details>
    <summary>
        <img src="https://easytripai.com/AI-Trip-Planner.jpg" alt="Trip Planner Page" />
    </summary>
   Demonstrates the quiz to determine user travel personality (pace, interests, budget).
   </details>

---

## 5. Challenges & Solutions

1. **SSR & API Routes Conflict**  
   - **Challenge:** Combining server-side rendering with AI-based routes and dynamic environment variables.  
   - **Solution:** Leveraged Next.js (App Router) for integrated `/api/` endpoints. Configured environment variables in `.env.local` on the server.

2. **Managing Private Keys & Confidential Data**  
   - **Challenge:** Keeping OpenAI keys out of the public repository.  
   - **Solution:** Stored keys in private `.env.local` and maintained a **private** GitHub repo.

3. **Drag-and-Drop Performance**  
   - **Challenge:** Smoothly reordering itinerary items without re-renders or data loss.  
   - **Solution:** Used DND Kit’s `PointerSensor` and `KeyboardSensor` with minimal state updates and stable keys.

4. **Map Coordinate Validation**  
   - **Challenge:** Ensuring that AI-provided coordinates are valid `[longitude, latitude]`.  
   - **Solution:** Created helper functions to validate, swap if needed, and filter out-of-range coordinates.

5. **Hosting & Deployment**  
   - **Challenge:** Deciding between static export or Node.js hosting for SSR.  
   - **Solution:** Deployed on a Node.js environment with SSH access to preserve API routes and SSR functionality.

---

## 6. Live Demo

### **Website:**  
[Easy Trip AI](https://easytripai.com/)

Visit the live app to:
1. **Generate** your travel personality with the built-in quiz.  
2. **Create** a custom trip itinerary with AI suggestions.  
3. **Discover** cultural insights and hidden gems.  
4. **Build** a packing list tailored to your itinerary.

---

## 7. Future Enhancements

1. **Social Sharing & Collaboration**  
   - Let users invite friends to view/edit the itinerary.
2. **Offline Mode**  
   - Cache itineraries for offline access when traveling.
3. **Multi-Language Support**  
   - Expand beyond English to offer the same experience in multiple languages.

---

## 8. Repository & Code Privacy

> The source code resides in a **private GitHub repository** to protect sensitive API keys and intellectual property.

- **If you’d like to explore the code**, please [reach out to me](mailto:akash@akashbuilds.com) for a read-only invite or a demo session.
- This ensures that proprietary logic and credentials remain **confidential**.

---

## 9. Contact

**Author:**  
[Akash Kumar](https://www.linkedin.com/in/theakashkumar/)  
Feel free to connect on **LinkedIn** or email me at **akash@akashbuilds.com** for questions or collaborations.

---

## 10. Conclusion

Easy Trip AI is a **feature-rich** travel planner leveraging the **power of AI**, a streamlined **user experience**, and a robust **tech stack**. It solves common pain points of travel planning by providing a single platform for **itinerary creation**, **cultural insights**, and **packing suggestions**, significantly reducing the overhead of trip organization.

**Thank you for viewing Easy Trip AI!**  
If you have any questions or want to learn more, feel free to reach out.
