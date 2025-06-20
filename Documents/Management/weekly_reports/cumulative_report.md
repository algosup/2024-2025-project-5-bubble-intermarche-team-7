# Cumulative Weekly Reports — Intermarché Pairing App  
**Team 7 – 2025**

---

## **Weekly Report — Week 1**
**Period:** April 22 – April 25, 2025  
*(Note: April 21 was public holiday.)*

### **Overview**
This week marked the launch of our Intermarché pairing app project. We kicked off with client alignment and laid the groundwork for design and data modeling. Due to concurrent Bubble training sessions, coding progress was minimal, focusing instead on planning and specification.

### **Accomplishments**
- **Client Kick‑off Meeting**: Aligned with the client on core user flows for an app where users start with a dish to find optimal wine & cheese pairings and designed with profitability in mind.
- **Requirements & Data Draft (All team)**: Defined page structure and sketched initial data types (Products shared across dishes, wines, cheeses).
- **Bubble Training**: Professional‑led tutorial to onboard the team on no‑code development practices.
- **Design & Mock‑ups**: Created Figma draft wireframes.
- **Functional Specification Draft**: Outlined key features.

### **Challenges**
- **No‑code Learning Curve**: Team members adjusted to Bubble.io in parallel with spec work, limiting hands‑on development time.
- **Time Constraints**: Only two weeks of course time were allocated; all setup and planning had to share the same window.

### **Plan for Next Week**
1. Progress Functional Specs (Quentin): Incorporate client feedback.
2. Data Modeling in Bubble (Manech): Implement the Products type, option sets (ProductType, DishCategory, TasteProfile, etc.), and the User.favorites field.
3. Component Development (Abderrazaq): Build and test TopNavbar and BottomNavbar as reusable elements.
4. Begin UI Implementation (Abderrazaq): Develop product cards (dishCards, wineCards, cheeseCards) and integrate search/filter logic.

### **Conclusion**
The foundational week established clear direction and ensured the team is ready to dive into Bubble development, with specs and designs in place to accelerate upcoming sprints.

---

## **Weekly Report — Week 2**
**Period:** April 28 – April 30, 2025  
*(Note: May 1–2 were public holidays.)*

### **Overview**
This week we continued our Bubble training most mornings; only two dedicated project sessions took place. With Pierre largely absent, focus shifted to UI design, page layouts, and initial logic drafts in Bubble.

### **Accomplishments**
- **Design Completion Figma (Quentin, Abderrazaq)**: Quentin and I finalized high‑fidelity designs for all screens: Home, Search, Recommendation, Favorites, Profile, Onboarding.
- **Bubble Page Layouts (Abderrazaq)**:  
  - Navigation Bars: built and styled TopNavbar & BottomNavbar reusable elements.  
  - Home Page: implemented header (topNavbar), footer (bottomNavbar), category card grid.  
  - Favorites Page: placed three reusable elements (dishCards, wineCards, cheeseCards) in a horizontal layout.
- **Static Components (Abderrazaq)**: Category cards on Home (image + label) in place. Product cards rendered correctly (static data) in Favorites and Home.
- **Technical Requirements Draft (Manech)**: Began drafting technical requirements document, establishing data types and naming conventions for the no-code Bubble implementation.

### **Challenges**
- **Developer Availability**: Pierre was absent much of the week, delaying workflow and search logic implementation.
- **Search Logic Pending**: SearchBox in TopNavbar and language toggle are styled but dynamic filter workflow is not yet configured.
- **Testing Resources**: Evan spent time on unrelated tasks; the Test Plan draft remains incomplete.

### **Plan for Next Week**
1. **Implement Search Workflow (Pierre)**: Configure SearchBox to filter `Products` by name in real time.
2. **Logic Integration (Pierre)**: Finish workflows for adding/removing favorites and filtering by tags.
3. **Test Plan Draft (Evan)**: Draft test cases for search, favorites, and navigation.
4. **Recommendation Logic (Pierre)**: Wire up Recommendation page to pull `recommended_*` lists and display them.
5. **One‑on‑one Check‑in (All team members)**: Ensure all team members have clear tasks and deadlines.

### **Conclusion**
Despite limited sessions and holidays, we advanced the app’s UI structure and Bubble data schema. Next week’s focus will be on workflow implementation and test‐case preparation to push toward a functional MVP.

---

## **Weekly Report — Week 3**
**Period:** May 5–9, 2025

### **Overview**
More project sessions this week as Bubble lessons concluded. Pierre joined only on Monday, then focused on another project. Design iterations continued, and logic for product cards and favorites started. Search logic was finally implemented, and database structure improved.

### **Accomplishments**
- **Search Logic**: SearchBox now filters products by name; live suggestions enabled.
- **Favorites Logic**: Product cards display dynamic favorite icons.
- **Profile Page**: Created and pre-filled.
- **Database**: Structure refined and imported CSV sample for test data.
- **Recommendation Page**: Structure started.

### **Challenges**
- **Team Engagement**: Pierre absent most of the week. Evan working separately, test plan not yet started.
- **Data Import**: CSV import postponed (Bubble free plan limitation).

### **Plan for Next Week**
- Implement full Recommendation workflow.
- Add logic for tag-based filtering.
- Start onboarding and translation features.
- Move forward with test plan drafting.

### **Conclusion**
Functional core is now visible in Bubble. As logic and UI link up, focus next week shifts to workflow polish and testing.

---

## **Weekly Report — Week 4**
**Period:** May 12–16, 2025

### **Overview**
Week 4 was slower in terms of team productivity, as only three project work sessions were scheduled. The team dynamic remained low, likely due to academic fatigue and upcoming summer break. Despite that, progress continued in small increments.

### **Accomplishments**
- **Functional Specification Submission (Quentin)**: Quentin is finalizing the functional specification for the May 16 deadline.
- **Design Iteration (Abderrazaq)**: Continued refining UI components: layout adjustments, spacing, responsive details. Fixed minor design issues across pages for consistency. Updated Figma mockups to reflect the current Bubble implementation.
- **Bubble Dev (Light)**: Worked on card component consistency (dish/wine/cheese). Started preparing the logic for tag displays on product cards.

### **Challenges**
- **Team Motivation**: The group dynamic remained flat with limited engagement. Most teammates were preoccupied with other school assignments or already in “vacation mode.”
- **Time Constraints**: Only 3 active project sessions were possible this week.

### **Plan for Next Week**
1. **Product Page**: Create a dedicated page to view all products filtered by type (wine, cheese, dish).
2. **Tag System**: Display information widgets directly on product cards (cheese type, AOP, IGP). Route clicks to filtered pages based on tag type.

### **Conclusion**
Although week 4 lacked momentum due to academic obligations and low engagement, essential progress was made in design polish and tag logic planning. A focused push will be needed in the coming week to resume full productivity ahead of the final presentation.

---

## **Weekly Report — Week 5**
**Period:** May 19–23, 2025

### **Overview**
Marked progress on tag filtering logic and onboarding. Recommendation page built; dynamic logic started. UI improved with new language dropdown and early onboarding flow. Sample products added to test features.

### **Accomplishments**
- **Filtering by Tags**: Implemented for dishes; started for wines/cheeses.
- **Recommendation Page**: Displays recommended wines/cheeses per dish.
- **Onboarding**: Initial pages built; language dropdown added.
- **Sample Data**: 1 sample dish, wine, cheese for testing.

### **Challenges**
- **Recommendation Logic**: Infinite recursion by design—navigating between related products.
- **Team Participation**: Most tasks handled by Abderrazaq.

### **Plan for Next Week**
- Extend tag filtering to wines and cheeses.
- Complete responsive fixes.
- Start database population (CSV with 30 dishes, 10 wines, 10 cheeses).
- Refine naming for search optimization.
- Finish repeating group logic for search.

### **Conclusion**
Key features in place, but much remains to refine search, data import, and polish.

---

## **Weekly Report — Week 6**
**Period:** May 26–28, 2025  
*(May 29–30 were public holidays.)*

### **Overview**
Week 6 focused on broadening filter logic and UI polish. Completed dynamic tag filtering for all product types. Database work began; technical delivered by Manech. Added “View All” buttons and search navigation improvements.

### **Accomplishments**
- **Tag Filtering**: Completed for wines and cheeses.
- **Responsive Fixes**: Various improvements.
- **Database Draft**: CSV for dishes, wines, cheeses; search-optimized names.
- **“View All” Buttons**: Route to respective all-items page.
- **Search RG Logic**: Repeating group display in search finished.
- **Technical Specification**: Delivered by Manech.

### **Challenges**
- **Translation**: Pending.
- **Image Import**: Delayed—will use trial before presentation.

### **Plan for Next Week**
- Database population and images.
- Finish translations and “view all” logic.
- Prepare for final import.

### **Conclusion**
Productive short week. Focus shifts to content and final database/image setup.

---

## **Weekly Report — Week 7**
**Period:** June 2–6, 2025

### **Overview**
Only 3 project sessions. Development pace slowed but ahead of schedule. Translation work begun. Database CSV finalized (50 images to find/compress). Import pending Bubble trial. Minor design changes.

### **Accomplishments**
- **Database**: Finished dish, wine, cheese CSVs.
- **Translation**: Started localization; not complete.
- **Test Plan**: Delivered by Evan (June 6).
- **Design**: No major changes; UI stabilized.

### **Challenges**
- **Bubble Free Plan**: Limits on import; trial will unlock before presentation.
- **Team Pace**: Slower, but manageable.

### **Plan for Next Week**
- Complete translation.
- Compress/import images.
- Import all data into Bubble.

### **Conclusion**
Database and planning on track; localization and image optimization to finish.

---

## **Weekly Report — Week 8**
**Period:** June 10–13, 2025  
*(June 09 was public holiday.)*

### **Overview**
Week 8 marked the final push toward project completion. With Monday being a public holiday, the remaining days were fully dedicated to development. Most features and content are now finalized, setting the stage for our final preparations.

### **Accomplishments**
- **Localization**: Completed translation (French/English); language dropdown added.
- **Media Optimization**: Images compressed, resized, and delivered responsively.
- **Database Import**: Imported full product data (30 dishes, 10 wines, 10 cheeses). Verified slugs, categories, relationships.
- **UI Enhancements**: Added splash screen, loading page, fully redesigned homepage.
- **Functionality**: Finalized all platform logic (search, filtering, navigation, recommendations, profile, favorites, etc).

### **Challenges**
- **Uneven Workload**: Majority handled by one member, but educational.
- **Project Fatigue**: Some teammates disengaged as deadline neared.

### **Plan for Next Week**
1. Final Testing & QA: Product walkthrough on Friday and Monday before deadline (23:59).
2. Presentation Preparation: Slide content, story, rehearsal for June 20.

### **Conclusion**
Despite challenges and imbalances, Week 8 was productive and rewarding. Product is functionally/visually complete; last week for polish and presentation.

---

## **Weekly Report — Week 9**
**Period:** June 16–20, 2025

### **Overview**
The final week of the project. All features were finalized and thoroughly tested. Slides and oral presentation rehearsed. Team delivered the final pitch on June 20.

### **Accomplishments**
- **Final QA**: Full walkthrough and bug checks.
- **Presentation**: All slides, speaker notes, and storytelling finalized and rehearsed.
- **Oral Defense**: Delivered June 20; smooth delivery and positive feedback.

### **Challenges**
- **Deadline Pressure**: Last-minute polish required rapid coordination.
- **Fatigue**: Team pushed hard to the end.

### **Conclusion**
The project closed with a successful presentation and a complete product. Teamwork, perseverance, and strong final sprints enabled us to deliver a product we are proud of.

---