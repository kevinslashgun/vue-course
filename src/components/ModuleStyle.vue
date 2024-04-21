<template>
    <h1 :class="myClasses['m-class']">Using Module CSS with name (kebab-case)</h1>
    <h1 :class="myClasses.anotherClass">Using Module CSS with name (camelCase)</h1>
    <h1 :class="$style['m-class2']">Using Module CSS with $ syntax (kebab-case)</h1>
    <h1 :class="$style.anotherClass2">Using Module CSS with $ syntax (camelCase)</h1>
</template>

<style module="myClasses">
/* kebab-case */
.m-class {
    background-color: firebrick;
    color: white;
}

/* camelCase */
.anotherClass {
    background-color: seagreen;
    color: white;
}
</style>

<style module>
.m-class2 {
    background-color: darkorange;
    color: white;
}

.anotherClass2 {
    background-color: darkslategray;
    color: white;
}
</style>