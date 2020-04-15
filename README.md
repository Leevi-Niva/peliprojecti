<!DOCTYPE html>
<html>
<head>
    <title>Calculator</title>
</head>
<body>

<style>
    .calculator-body {
        background-color: #CCCCCC;
        max-width: 300px;
        margin: 0 auto;
    }

    form {
        margin: 0 auto;
        max-width: 960px;
        text-align: center;
    }

    #screen {
        padding: 5px;
        font-size: 22px;
        position: relative;
    }
</style>

<?php



    $number = $_POST['number'];
    $op = $_POST['op'];
    $ops = $_POST['ops'];
    $store = $_POST['store'];
    $screen = $_POST['screen'];
    $ans = $_POST['equal'];

    if (isset($_POST['screen'])) {
        $screen = $number;
        $screen = $ans;
    }

    if (isset($_POST['op'])) {
        $ops = $op;
        $screen .= $ops;
        $ans += $number;
    }

    if (isset($_POST['number'])) {
        $screen = $number;
        $number = $screen;
//        $number .= $tore;
    }
    //    $screen .= $ans;
    if (isset($_POST['equal'])) {
        $ans = $number + $op + $ans;

        //    if(isset($_POST['equal']))
        //    {
        switch ($op) {
            case '-':
                $ans = $number - $ans;
                //                $screen = $ans;
                break;

            case '+':
                $ans = $number + $ans;
                //                $screen = $ans;
                break;

            case '*':
                $ans = $number * $ans;
                break;
        }
    }
?>

<form action="" method="post">
    <div class="calculator-body calculator">
        <div class="screen-wrapper">
            <input type="text" id="screen" name="screen" value="<?php echo $screen; ?>">
        </div>
        <div class="column">
            <input type="reset" value="c" name="op" id="clear">
            <input type="submit" value="del" name="op" id="backspace"/>
        </div>
        <div class="column">
            <input type="submit" value="7" name="number"/>
            <input type="submit" value="8" name="number"/>
            <input type="submit" value="9" name="number"/>
            <input type="submit" value="/" name="op" id="divide"/>
        </div>
        <div class="column">
            <input type="submit" value="4" name="number"/>
            <input type="submit" value="5" name="number"/>
            <input type="submit" value="6" name="number"/>
            <input type="submit" value="*" name="op" id="multiply"/>
        </div>
        <div class="column">
            <input type="submit" value="1" name="number"/>
            <input type="submit" value="2" name="number"/>
            <input type="submit" value="3" name="number"/>
            <input type="submit" value="-" name="op" id="subtract"/>
        </div>
        <div class="column">
            <input type="submit" value="0" name="number"/>
            <input type="submit" value="." name="number" id="dot"/>
            <input type="submit" value="=" name="equal" id="equal"/>
            <input type="submit" name="op" value="+" id="plus"/>
        </div>
        <input type="text" value="<?php echo $ops; ?>" name="ops"/>
        <input type="text" value="<?php echo $ans; ?>" name="store"/>
        <input type="text" value="<?php echo $ans; ?>" name="equal"/>
</form>
</body>
</html>
