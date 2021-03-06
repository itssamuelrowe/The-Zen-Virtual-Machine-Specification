## Chapter 1: Introduction
 * History of Zen
 * The Zen Virtual Machine

## Chapter 2: Architecture
 * The Constant Pool

## Chapter 3: Binary Entity Format (FEB)
 * The Constant Pool Format

## Chapter 4: Entity Loader Module
## Chapter 5: Entity Linker Module
## Chapter 6: Entity Initializer Module
## Chapter 7: Instruction Set
Section 7.1 Instruction Nomenclature  
Section 7.2 Insructions  
* Section 7.2.1 - nop
* Section 7.2.2 - add_i
* Section 7.2.3 - add_l
* Section 7.2.4 - add_f
* Section 7.2.5 - add_d
* Section 7.2.6 - and_i
* Section 7.2.7 - and_l
* Section 7.2.8 - or_i
* Section 7.2.9 - or_l
* Section 7.2.10 - shift_left_i
* Section 7.2.11 - shift_left_l
* Section 7.2.12 - shift_right_i
* Section 7.2.13 - shift_right_l
* Section 7.2.14 - shift_right_ui
* Section 7.2.15 - shift_right_ul
* Section 7.2.16 - xor_i
* Section 7.2.17 - xor_l
* Section 7.2.18 - cast_itb
* Section 7.2.19 - cast_its
* Section 7.2.20 - cast_itl
* Section 7.2.21 - cast_itf
* Section 7.2.22 - cast_itd
* Section 7.2.23 - cast_ltb
* Section 7.2.24 - cast_lts
* Section 7.2.25 - cast_lti
* Section 7.2.26 - cast_ltf
* Section 7.2.27 - cast_ltd
* Section 7.2.28 - cast_fti
* Section 7.2.29 - cast_ftl
* Section 7.2.30 - cast_ftd
* Section 7.2.31 - cast_dti
* Section 7.2.32 - cast_dtl
* Section 7.2.33 - cast_dtf
* Section 7.2.34 - cast_itc
* Section 7.2.35 - check_cast
* Section 7.2.36 - compare_l
* Section 7.2.37 - compare_lt_f
* Section 7.2.38 - compare_gt_f
* Section 7.2.39 - compare_lt_d
* Section 7.2.40 - compare_gt_d
* Section 7.2.41 - divide_i
* Section 7.2.42 - divide_l
* Section 7.2.43 - divide_f
* Section 7.2.44 - divide_d
* Section 7.2.45 - duplicate
* Section 7.2.46 - duplicate_x1
* Section 7.2.47 - duplicate_x2
* Section 7.2.48 - duplicate2
* Section 7.2.49 - duplicate2_x1
* Section 7.2.50 - duplicate2_x2
* Section 7.2.51 - jump_eq0_i
* Section 7.2.52 - jump_ne0_i
* Section 7.2.53 - jump_lt0_i
* Section 7.2.54 - jump_gt0_i
* Section 7.2.55 - jump_le0_i
* Section 7.2.56 - jump_ge0_i
* Section 7.2.57 - jump_eq_i
* Section 7.2.58 - jump_ne_i
* Section 7.2.59 - jump_lt_i
* Section 7.2.60 - jump_gt_i
* Section 7.2.61 - jump_le_i
* Section 7.2.62 - jump_ge_i
* Section 7.2.63 - jump_eq_a
* Section 7.2.64 - jump_ne_a
* Section 7.2.65 - jump_eqn_a
* Section 7.2.66 - jump_nen_a
* Section 7.2.67 - increment_i
* Section 7.2.68 - invoke_special
* Section 7.2.69 - invoke_virtual
* Section 7.2.70 - invoke_dynamic
* Section 7.2.71 - invoke_static
* Section 7.2.72 - jump
* Section 7.2.73 - load_i
* Section 7.2.74 - load_l
* Section 7.2.75 - load_f
* Section 7.2.76 - load_d
* Section 7.2.77 - load_i0
* Section 7.2.78 - load_i1
* Section 7.2.79 - load_i2
* Section 7.2.80 - load_i3
* Section 7.2.81 - load_l0
* Section 7.2.82 - load_l1
* Section 7.2.83 - load_l2
* Section 7.2.84 - load_l3
* Section 7.2.85 - load_f0
* Section 7.2.86 - load_f1
* Section 7.2.87 - load_f2
* Section 7.2.88 - load_f3
* Section 7.2.89 - load_d0
* Section 7.2.90 - load_d1
* Section 7.2.91 - load_d2
* Section 7.2.92 - load_d3
* Section 7.2.93 - load_a0
* Section 7.2.94 - load_a1
* Section 7.2.95 - load_a2
* Section 7.2.96 - load_a3
* Section 7.2.97 - load_ab
* Section 7.2.98 - load_ac
* Section 7.2.99 - load_as
* Section 7.2.100 - load_ai
* Section 7.2.101 - load_al
* Section 7.2.102 - load_af
* Section 7.2.103 - load_ad
* Section 7.2.104 - load_aa
* Section 7.2.105 - load_instance_field
* Section 7.2.106 - load_static_field
* Section 7.2.107 - load_cpr
* Section 7.2.108 - load_array_size
* Section 7.2.109 - modulo_i
* Section 7.2.110 - modulo_l
* Section 7.2.111 - modulo_f
* Section 7.2.112 - modulo_d
* Section 7.2.113 - multiply_i
* Section 7.2.114 - multiply_l
* Section 7.2.115 - multiply_f
* Section 7.2.116 - multiply_d
* Section 7.2.117 - negate_i
* Section 7.2.118 - negate_l
* Section 7.2.119 - negate_f
* Section 7.2.120 - negate_d
* Section 7.2.121 - new
* Section 7.2.122 - new_array
* Section 7.2.123 - new_array_a
* Section 7.2.124 - new_array_an
* Section 7.2.125 - pop
* Section 7.2.126 - pop2
* Section 7.2.127 - push_null
* Section 7.2.128 - push_in1
* Section 7.2.129 - push_i0
* Section 7.2.130 - push_i1
* Section 7.2.131 - push_i2
* Section 7.2.132 - push_i3
* Section 7.2.133 - push_i4
* Section 7.2.134 - push_i5
* Section 7.2.135 - push_l0
* Section 7.2.136 - push_l1
* Section 7.2.137 - push_l2
* Section 7.2.138 - push_f0
* Section 7.2.139 - push_f1
* Section 7.2.140 - push_f2
* Section 7.2.141 - push_d0
* Section 7.2.142 - push_d1
* Section 7.2.143 - push_d2
* Section 7.2.144 - push_b
* Section 7.2.145 - push_s
* Section 7.2.146 - return
* Section 7.2.147 - return_i
* Section 7.2.148 - return_l
* Section 7.2.149 - return_f
* Section 7.2.150 - return_d
* Section 7.2.151 - return_a
* Section 7.2.152 - rtti
* Section 7.2.153 - store_i
* Section 7.2.154 - store_i0
* Section 7.2.155 - store_i1
* Section 7.2.156 - store_i2
* Section 7.2.157 - store_i3
* Section 7.2.158 - store_l
* Section 7.2.159 - store_l0
* Section 7.2.160 - store_l1
* Section 7.2.161 - store_l2
* Section 7.2.162 - store_l3
* Section 7.2.163 - store_f
* Section 7.2.164 - store_f0
* Section 7.2.165 - store_f1
* Section 7.2.166 - store_f2
* Section 7.2.167 - store_f3
* Section 7.2.168 - store_d
* Section 7.2.169 - store_d0
* Section 7.2.170 - store_d1
* Section 7.2.171 - store_d2
* Section 7.2.172 - store_d3
* Section 7.2.173 - store_a
* Section 7.2.174 - store_a0
* Section 7.2.175 - store_a1
* Section 7.2.176 - store_a2
* Section 7.2.177 - store_a3
* Section 7.2.178 - store_ab
* Section 7.2.179 - store_ac
* Section 7.2.180 - store_as
* Section 7.2.181 - store_ai
* Section 7.2.182 - store_al
* Section 7.2.183 - store_af
* Section 7.2.184 - store_ad
* Section 7.2.185 - store_aa
* Section 7.2.186 - store_instance_field
* Section 7.2.187 - store_static_field
* Section 7.2.188 - subtract_i
* Section 7.2.189 - subtract_l
* Section 7.2.190 - subtract_f
* Section 7.2.191 - subtract_d
* Section 7.2.192 - swap
* Section 7.2.193 - switch_table
* Section 7.2.194 - switch_search
* Section 7.2.195 - throw
* Section 7.2.196 - wide

## Chapter 8: Internals of the Zen Compiler - Case Study 1
## Chapter 9: Internals of the Zen Virtual Machine - Case Study 2