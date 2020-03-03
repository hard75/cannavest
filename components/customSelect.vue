<template>
    <div>    
        <div class="dropdown">
            <div class="select">
                <span><i :class="icon"></i> {{ title }}</span>
                <i class="fas fa-sort-down"></i>
            </div>
            <input type="hidden" name="gender">
            <ul class="dropdown-menu">
                <li v-for="(item, i) in data" :key="i" :id="item.value"> {{ item.label }}</li>
            </ul>
        </div>
    
        <span class="msg"></span>
    </div>
</template>

<script>
export default {
    props: [ 'title', 'icon', 'data' ],
    methods: {
        initSelect () {
            /*Dropdown Menu*/
            $('.dropdown').click(function () {
                    $(this).attr('tabindex', 1).focus();
                    $(this).toggleClass('active');
                    $(this).find('.dropdown-menu').slideToggle(300);
                });
                $('.dropdown').focusout(function () {
                    $(this).removeClass('active');
                    $(this).find('.dropdown-menu').slideUp(300);
                });
                $('.dropdown .dropdown-menu li').click(function () {
                    $(this).parents('.dropdown').find('span').text($(this).text());
                    $(this).parents('.dropdown').find('input').attr('value', $(this).attr('id'));
                });
            /*End Dropdown Menu*/


            $('.dropdown-menu li').click(function () {
            var input = '<strong>' + $(this).parents('.dropdown').find('input').val() + '</strong>',
                msg = '<span class="msg">Hidden input value: ';
            $('.msg').html(msg + input + '</span>');
            }); 
        }
    },
    mounted () {
        this.initSelect();
    }
}
</script>

<style>

    span.msg,
    span.choose {
        color: #555;
        padding: 5px 0 10px;
        display: inherit
    }

    /*Styling Selectbox*/
    .dropdown {
        width: 182px;
        display: inline-block;
        background-color: #EDEDEE;
        border-radius: 5px;
        box-shadow: 0 0 2px rgb(204, 204, 204);
        transition: all .5s ease;
        position: relative;
        font-size: 18px;
        color: #807e7e;
        height: 100%;
        text-align: left;

        padding-top: 6px;
        padding-left: 6px;
    }


    .dropdown .select {
        cursor: pointer;
        display: block;
        padding: 10px;
        height: 30px;

        font-family: "adobe-clean", sans-serif;
    }

    .dropdown .select span {
        position: absolute;
        top: 20px;
    }

    .dropdown .select span > i {
        margin-right: 10px;
    }

    .dropdown .select > i {
        color: #888;
        cursor: pointer;
        transition: all .3s ease-in-out;
        float: right;
        line-height: 20px;
        font-size: 28px;

        padding-right: 5px;
    }
    .dropdown:hover {
        box-shadow: 0 0 4px rgb(204, 204, 204)
    }
    .dropdown:active {
        background-color: #f8f8f8
    }
    .dropdown.active:hover,
    .dropdown.active {
        box-shadow: 0 0 4px rgb(204, 204, 204);
        border-radius: 5px 5px 0 0;
        background-color: #f8f8f8
    }
    .dropdown.active .select > i {
        transform: rotate(180deg);
        padding-top: 10px;
    }
    .dropdown .dropdown-menu {
        position: absolute;
        background-color: #fff;
        width: 100%;
        left: 0;
        margin-top: 1px;
        box-shadow: 0 1px 2px rgb(204, 204, 204);
        border-radius: 0 1px 5px 5px;
        overflow: hidden;
        display: none;
        max-height: 144px;
        overflow-y: auto;
        z-index: 9
    }
    .dropdown .dropdown-menu li {
        padding: 10px;
        transition: all .2s ease-in-out;
        cursor: pointer;

        background-color:#EDEDEE;
    } 
    .dropdown .dropdown-menu {
        padding: 0;
        list-style: none
    }
    .dropdown .dropdown-menu li:hover {
        background-color: #f2f2f2
    }
    .dropdown .dropdown-menu li:active {
        background-color: #e2e2e2
    }
</style>