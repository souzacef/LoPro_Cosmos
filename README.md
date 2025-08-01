# LoPro_Cosmos keyboard

/*
 * Copyright (c) 2020 The ZMK Contributors
 *
 * SPDX-License-Identifier: MIT
 */

#define ZMK_POINTING_DEFAULT_MOVE_VAL 1500  // default: 600
#define ZMK_POINTING_DEFAULT_SCRL_VAL 20    // default: 10

#include <dt-bindings/zmk/pointing.h>
#include <behaviors.dtsi>
#include <dt-bindings/zmk/keys.h>
#include <dt-bindings/zmk/bt.h>
#include <dt-bindings/zmk/outputs.h>


#define DEFAULT 0
#define FUNCTION 1

/ {
	keymap {
		compatible = "zmk,keymap";

		default_layer {
			bindings = <			
			&kp GRAVE  &kp N1     &kp N2    &kp N3    &kp N4    &kp N5            &kp N6     &kp N7     &kp N8     &kp N9    &kp N0        &kp MINUS      
			&kp TAB    &kp Q      &kp W     &kp E     &kp R     &kp T             &kp Y      &kp U      &kp I      &kp O     &kp P         &kp LBKT        
			&kp CAPS   &kp A      &kp S     &kp D     &kp F     &kp G             &kp H      &kp J      &kp K      &kp L     &kp SEMI      &kp APOS        
            &kp LSHFT  &kp Z      &kp X     &kp C     &kp V     &kp B             &kp N      &kp M      &kp COMMA  &kp DOT   &kp SLASH     &kp LC(LA(W))   
			&kp N6     &kp N7     &kp N8    &kp N9    &kp HOME  &kp DEL           &kp ENTER  &kp BSPC   &kp SPACE  &kp LEFT  &kp RIGHT     &kp RWIN       
			&kp DOWN   &kp LCTRL  &kp LWIN  &kp LALT  &kp UP    &kp SPACE         &kp BSPC   &kp ENTER  &kp DEL    &kp END   &mo FUNCTION  &kp N1            
			>;
		};
		
		functions_layer {
			bindings = <
			&bt BT_SEL 0  &bt BT_SEL 1  &bt BT_SEL 2    &bt BT_SEL 3    &bt BT_SEL 4     &out OUT_TOG        &bt BT_CLR	 &kp C_PP         &kp KP_EQUAL  &kp KP_SLASH  &kp KP_MULTIPLY  &none         
			&sys_reset    &bootloader   &studio_unlock  &none           &none            &none               &none       &kp C_VOL_UP     &trans        &trans        &trans           &studio_unlock
			&none         &none         &none           &mmv MOVE_UP    &none            &none               &none       &kp C_VOL_DN     &kp N4        &kp N5        &kp N6           &kp KP_MINUS   
			&none  	      &none         &mmv MOVE_LEFT  &mmv MOVE_DOWN  &mmv MOVE_RIGHT  &none               &none       &kp PAUSE_BREAK  &kp N1        &kp N2        &kp N3           &kp KP_PLUS    
            &none         &none         &none           &none           &none            &none               &none       &kp PSCRN        &kp N0        &trans        &trans           &none   	      
			&none         &none         &none           &none           &none            &none               &none       &none            &none         &none         &none            &none          
			     
			>;
		};
	};

	
};

/ {
    bt-cosmo {
        compatible = "zmk,bluetooth";
        local-name = "LoPro Cosmos";
    };
};