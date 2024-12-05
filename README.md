# React Tabs with Router

Implemented the `App` with `Home` page available at `/` and `Tabs` page available
at `/tabs`. Each page should have the correct title `Home page` or `Tabs page`.

1. Navigation with `Home` and `Tabs` links:
    - should be visible on every page;
    - should highlight an active link with `is-active` class;
1. `TabsPage` page should work for both `/tabs` and `/tabs/:tabId` paths (use nested routes);
    ```tsx
    <Route path="tabs">
      <Route index element={<TabsPage />} />
      <Route path=":tabId" element={<TabsPage />} />
    </Route>
    ```
1. Each tab should update the URL on click.
    - the URL should follow the next format `/tabs/:tabId` (use actual `tab.id` instead of `:tabId`);
    - replace `<a href="#...">` with `<Link to="/tabs/...">` and remove `onClick`;
    - **don't** use `NavLink` as `is-active` class is added to a parent element;
    - read `tabId` from the URL using [useParams](https://reactrouter.com/en/main/hooks/use-params) hook;
    - if the `tabId` does not match any tab show `Please select a tab` message instead of a tab content.
1. The page should show the same content after a reload.
1. Redirect from `/home` to `/` using the [Navigate](https://reactrouter.com/en/main/components/navigate) component;
1. Show the `Page not found` title for all the other URLs;

## Demo Links

- [DEMO LINK](https://AndriiZakharenko.github.io/react_tabs-with-router/)


