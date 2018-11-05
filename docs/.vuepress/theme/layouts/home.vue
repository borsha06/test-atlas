<template><va-layout-manager>
<va-page>
    <va-page-header>...</va-page-header>
    <article>
        <p class="post-page-meta">
            {{ postDate }}
        </p>
    </article>
 Welcome
    <va-table :hover="hover" :size="size">
        <table>
            <thead>
            <tr>
                <th>Heading 1</th>
                <th>Heading 2</th>
                <th>Heading 3</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>Row 1, column 1</td>
                <td>Row 1, column 2</td>
                <td>Row 1, column 3</td>
            </tr>
            <tr>
                <td>Row 2, column 1</td>
                <td>Row 2, column 2</td>
                <td>Row 2, column 3</td>
            </tr>
            <tr>
                <td>Row 3, column 1</td>
                <td>Row 3, column 2</td>
                <td>Row 3, column 3</td>
            </tr>
            <tr>
                <td>Row 4, column 1</td>
                <td>Row 4, column 2</td>
                <td>Row 4, column 3</td>
            </tr>
            </tbody>
        </table>
    </va-table>
</va-page>
</va-layout-manager>
</template>
<script>
    export default {
        data() {
            return {
                hover: true,
                size: 'lg',
                postDate: '12/06/2018'
            }
        }
    }
</script>