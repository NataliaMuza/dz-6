package org.example;

import java.util.ArrayList;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

public class App
{
    public static void main(String[] args) {

    // Завдання 1
        // Ініціалізація масиву міст
        String[] cities = new String[]{"Lviv", "Vinnytcia", "Kyiv", "London"};
        // Рядок для пошуку
        String searchCity = "Vinnytcia";

        // Вивід списку через масив for
        for (int i = 0; i < cities.length; i++) {
            System.out.println(cities[i]);
        }
        System.out.println();

        // Вивід списку через масив forEach
        for (String city : cities) {
            System.out.println(city);
        }
        System.out.println();

        // Функція для пошуку елемента в масиві та виведення результату
        boolean result = findStringInArray(cities, searchCity);
        System.out.println("Vinnytcia: " + result);
        System.out.println();

    //Завдання 2
        // Список міст з повтореннями
        ArrayList<String> cityList = new ArrayList<>();
        cityList.add("Vinnytcia");
        cityList.add("Lviv");
        cityList.add("Lviv");
        cityList.add("Kyiv");
        cityList.add("London");

        for (String city : cityList) {
            System.out.println(city);
        }
        System.out.println();

        // Видалення повторень та друк результату
        Set<String> uniqueCities = removeDuplicates(cityList);
        System.out.println("Unique cities: " + uniqueCities);

    }

    // Функція для пошуку рядка у масиві
    public static boolean findStringInArray(String[] array, String searchString) {
        for (String string : array) {
            if (string.equals(searchString)) {
                return true;
            }
        }
        return false;
    }

    // Функція для видалення повторень з List
    public static Set<String> removeDuplicates(List<String> list) {
        // Перетворення List у Set для видалення повторень
        Set<String> set = new HashSet<>(list);
        System.out.println("Set after removing duplicates: " + set);
        System.out.println();
        return set;
    }
//    // Функція для перетворення рядка на масив символів
//    public static char[] convertStringToCharArray(String str) {
//        return str.toCharArray();
//    }
}