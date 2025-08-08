<template>
    <div>
        <div class="p-1">
            <strong>Tên:</strong>
            {{ staff.HoTenNV }}
        </div>
        <div class="p-1">
            <strong>Chức vụ:</strong>
            {{ staff.ChucVu }}
        </div>
        <div class="p-1">
            <strong>Địa chỉ:</strong>
            {{ staff.DiaChi }}
        </div>
        <div class="p-1">
            <strong>Điện thoại:</strong>
            {{ staff.SoDienThoai }}
        </div>
        <div class="mt-3">
            <button class="btn btn-warning btn-sm" @click="goToEdit">
                <i class="fas fa-edit"></i> Hiệu chỉnh
            </button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        staff: { type: Object, required: true },
    },
    methods: {
        goToEdit() {
            this.$router.push({ name: "staff.edit", params: { id: this.staff._id } });
        },
    },
};
</script>
