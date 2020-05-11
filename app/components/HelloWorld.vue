<template>
    <Page>
        <ActionBar title="Tip Calculator" />
        <ScrollView>
            <StackLayout class="home-panel">
                <TextField v-model="textFieldValue"
                    hint="Enter Bill Amount..." />
                <Button text="Submit" @tap="isHidden = true" backgroundColor="#ADD8E6" />
                <TextView editable="false">
                    <FormattedString>
                        <Span text="Tip him..... " v-if="isHidden"
                            fontSize="medium" />
                        <Span v-if="isHidden" :text="textFieldValue/10"
                            fontSize="medium" />
                    </FormattedString>
                </TextView>
            </StackLayout>
        </ScrollView>
    </Page>
</template>

<script>
    export default {
        data() {
            return {
                textFieldValue: "",
                isHidden: false
            };
        }
    };
</script>

<style scoped>
    .home-panel {
        vertical-align: center;
        font-size: 20;
        margin: 15;
    }

    .description-label {
        margin-bottom: 15;
    }
</style>