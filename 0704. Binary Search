/**
 * Given an array of integers nums which is sorted in ascending order, and an integer target, write a function to search target in nums. 
 * If target exists, then return its index. Otherwise, return -1.
 * You must write an algorithm with O(log n) runtime complexity.
 */
int search(int* nums, int numsSize, int target){
    if(numsSize == 0 || !nums){
        return -1;
    }
    
    int target_index = numsSize >> 1;
    int upper_bound = numsSize - 1;
    int lower_bound = 0;
    int tmp = 0;

    if(nums[upper_bound] < target){
        return -1;
    }
    else if(nums[upper_bound] == target){
        return upper_bound;
    }
    
    if(nums[lower_bound] > target){
        return -1;
    }
    else if(nums[lower_bound] == target){
        return lower_bound;
    }
    do{
        if(nums[target_index] == target){
            return target_index;
        }
        else{
            if(nums[target_index] < target){
                tmp = (target_index + upper_bound) >> 1;
                lower_bound = target_index;
            }
            else{
                tmp = (target_index + lower_bound) >> 1;
                upper_bound = target_index;
            }
            if(((lower_bound == target_index) && (target_index == upper_bound)) || (upper_bound - lower_bound == 1)){
                return -1;
            }
            target_index = tmp;
        }
    }while(1);
    return -1;
}
