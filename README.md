# Factory-Engine-F-A---18C
Mach 2.5 with AfterBurner



Voici les modifications du code : 


```java

SFM_Data = {
        aerodynamics = {
            Cy0 = 0,
            Mzalfa = 4.355,
            Mzalfadt = 0.8,
            kjx = 2.75,
            kjz = 0.00125,
            Czbe = -0.016,
            cx_gear = 0.0268,
            cx_flap = 0.23,
            cy_flap = 0.79,
            cx_brk = 0.08,
            table_data = {
                [1] = {0.0,  0.015, 0.07,  0.134, 0.0567, 0.5, 30, 2.4},
                [2] = {0.2,  0.0154, 0.07,  0.134, 0.056,  1.5, 30, 2.4},
                [3] = {0.4,  0.0156, 0.07,  0.134, 0.0549, 2.5, 30, 2.4},
                [4] = {0.6,  0.0164, 0.073, 0.134, 0.0474, 3.5, 30, 2.4},
                [5] = {0.8,  0.0201, 0.079, 0.144, 0.0607, 3.5, 27.333, 2.32},
                [6] = {1.0,  0.020,  0.085, 0.219, 0.0812, 3.5, 24.666, 2.24},
                [7] = {1.4,  0.016,  0.062, 0.468, 0.0751, 1.625, 14.5, 1.9}, -- Réduction à Mach 1.4
                [8] = {2.0,  0.012,  0.054, 0.545, 0.0708, 1.5, 13, 1.8}, -- Réduction à Mach 2
                [9] = {2.5,  0.010,  0.046, 0.622, 0.0665, 1.2, 12.5, 1.6}, -- Réduction à Mach 2.5
                [10] = {3.0, 0.009,  0.039, 0.743, 0.0618, 0.9, 12, 1.4},
            },
        },
        engine = {
            type = "TurboFan",
            Nmg = 64.1,
            Nominal_RPM = 16810.0,
            Nominal_Fan_RPM = 13270.0,
            Startup_Duration = 33.0,
            MinRUD = 0.1,
            MaxRUD = 1.0,
            MaksRUD = 0.85,
            ForsRUD = 0.91,
            hMaxEng = 19,
            dcx_eng = 0.0144,
            cemax = 1.3, -- Consommation maximale (sec)
            cefor = 2.7, -- Consommation postcombustion
            dpdh_m = 5000, -- Poussée en sec diminue plus lentement
            dpdh_f = 8000, -- Poussée postcombustion diminue plus lentement
            table_data = {
                [1] = {0,    50000, 130000}, -- Au sol
                [2] = {0.2,  52000, 135000}, 
                [3] = {0.4,  60000, 140000},
                [4] = {0.6,  70000, 145000},
                [5] = {0.8,  80000, 150000},
                [6] = {1.0,  85000, 155000},
                [7] = {1.2,  90000, 160000}, -- Atteint Mach 1.2 sans PC
                [8] = {1.4,  70000, 165000}, -- Limite en sec
                [9] = {1.6,  40000, 170000}, -- Transition en PC
                [10] = {1.8, 20000, 175000},
                [11] = {2.0, 15000, 180000},
                [12] = {2.2, 10000, 185000},
                [13] = {2.5, 5000, 190000}, -- Atteint Mach 2.5 en PC
                [14] = {2.8, 2000, 150000},
                [15] = {3.0, 1000, 120000},
            },
        },
    }
    ```