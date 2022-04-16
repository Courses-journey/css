## 01

```
/* Any Element With Class Title */
.title {
}

/* id */
#nav {
}

/* div element */
div {
}

/* h2 element */
h2 {
}
```

----------

## 02

```
<!-- external -->
<link rel="stylesheet" href="css/file.css" />

<!-- enternal -->
<style>
p {
  color: red;
}
</style>

<!-- inline -->
<p style="color: blue;">This Is Our Paragraph</p>
```

----------

## 03

```
<!-- Write Path -->
<link rel="stylesheet" href="assets/css/master.css" />
```

----------

## 04

```
<!-- Write Path -->
<link rel="stylesheet" href="../source/css/master.css" />
```

----------

## 05

```
/* valid */
._user-name {
}

/* valid */
.-user-name {
}

/* valid */
.-user-name {
}

/* not valid */
.1user-name {
}

/* not valid */
.@user-name {
}

/* not  valid */
.user@name {
}

/* valid */
._user10name {
}

/* valid */
.u {
}
```

----------

## 05

```
/* not */
.USERNAME {
}

/* not */
.UserName {
}

/* best */
.user-name {
}

/* not */
.userName {
}

/* not */
.usernameprofile {
}
```