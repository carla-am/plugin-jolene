# plugin-jolene
plugin wp de jolene de dolly parton

<?php
/** 
* @package Hello_Jolene
* @version 1.0
*/
/*
Plugin Name: Hello Jolene
Plugin URI:
Description: plugin de citas coa canción de Dolly Parton 'Jolene'
Author: carla am
Version: 1.0
Author URI:
*/

function jolene_lyrics() {
    // letra jolene
    $lyrics = "Jolene, Jolene, Jolene, Jolene
    I'm begging of you, please, don't take my man
    Jolene, Jolene, Jolene, Jolene
    Please, don't take him just because you can
    Your beauty is beyond compare
    With flaming locks of auburn hair
    With ivory skin and eyes of emerald green
    Your smile is like a breath of spring
    Your voice is soft like summer rain
    And I cannot compete with you, Jolene
    He talks about you in his sleep
    There's nothing I can do to keep
    From crying when he calls your name, Jolene
    And I can easily understand
    How you could easily take my man
    But you don't know what he means to me, Jolene
    Jolene, Jolene, Jolene, Jolene
    I'm begging of you, please, don't take my man
    Jolene, Jolene, Jolene, Jolene
    Please, don't take him just because you can
    You could have your choice of men
    But I could never love again
    He's the only one for me, Jolene
    I had to have this talk with you
    My happiness depends on you
    And whatever you decide to do, Jolene
    Jolene, Jolene, Jolene, Jolene
    I'm begging of you, please, don't take my man
    Jolene, Jolene, Jolene, Jolene
    Please, don't take him even though you can
    Jolene
    Jolene
    ";

    $lyrics = explode("\n", $lyrics);
    /* explode é uma funçao para colher cada linha
    converte cada linha num array */
    return wptexturize($lyrics[mt_rand( 0, count($lyrics) - 1 )]);
    /*randoniza a selecçao de linha*/
}

add_shortcode('jolene', 'jolene_lyrics');
