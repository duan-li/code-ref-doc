<?php if (!defined('BASEPATH')) exit('No direct script access allowed');

class Migration_Initial_tables extends Migration {

    public function up()
    {
        $sql = array();

        // Ribbits
        $sql[] = "CREATE TABLE ribbits (
                id            INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
                user_id    INT(11) UNSIGNED NOT NULL,
                ribbit        VARCHAR(140),
                created_at    DATETIME,
                PRIMARY KEY(id, user_id)
            );";

        // Follows
        $sql[] = "CREATE Table follows (
                id            INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
                user_id       INT(11) UNSIGNED NOT NULL,
                followee_id   INT(11) UNSIGNED NOT NULL,
                PRIMARY KEY(id, user_id)
            );";

        foreach ($sql as $s)
        {
            $this->db->query($s);
        }
    }

    //--------------------------------------------------------------------

    public function down()
    {
        $this->dbforge->drop_table('ribbits');
        $this->dbforge->drop_table('follows');
    }

    //--------------------------------------------------------------------

}