<?php if (!defined('BASEPATH')) exit('No direct script access allowed');

class Ribbit_model extends MY_Model {

    protected $table_name   = 'ribbits';
    protected $date_format  = 'datetime';

    protected $log_user             = true;
    protected $set_created          = true;
    protected $created_on_field     = 'created_at';
    protected $created_by_field     = 'user_id';

    //--------------------------------------------------------------------
}