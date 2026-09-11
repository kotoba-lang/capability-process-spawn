(ns kotoba.capability.process.spawn-test
  (:require [clojure.test :refer [deftest is]]
            [kotoba.capability.process.spawn :as spawn]))

(deftest manifest-identity
  (is (= "process/spawn" (:capability/id spawn/manifest)))
  (is (= :contract-only (:capability/provider-status spawn/manifest)))
  (is (contains? (:capability/imports spawn/manifest) :process-spawn)))
