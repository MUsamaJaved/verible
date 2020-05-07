---
---

# `verilog_format`

Tool for formatting Verilog and SystemVerilog code. Part of the verible tool
suite.

## Command line arguments
```
verilog_format: usage: bazel-bin/verilog/tools/formatter/verilog_format [options] <file>
To pipe from stdin, use '-' as <file>.

  Flags from external/com_google_absl/absl/flags/parse.cc:
    --flagfile (comma-separated list of files to load flags from); default: ;
    --fromenv (comma-separated list of flags to set from the environment [use
      'export FLAGS_flag1=value']); default: ;
    --tryfromenv (comma-separated list of flags to try to set from the
      environment if present); default: ;
    --undefok (comma-separated list of flag names that it is okay to specify on
      the command line even if the program does not define a flag with that
      name); default: ;


  Flags from external/com_google_absl/absl/flags/internal/usage.cc:
    --help (show help on important flags for this binary [tip: all flags can
      have two dashes]); default: false;
    --helpfull (show help on all flags); default: false; currently: true;
    --helpmatch (show help on modules whose name contains the specified substr);
      default: "";
    --helpon (show help on the modules named by this flag value); default: "";
    --helppackage (show help on all modules in the main package);
      default: false;
    --helpshort (show help on only the main module for this program);
      default: false;
    --only_check_args (exit after checking all flags); default: false;
    --version (show version and build info and exit); default: false;


  Flags from verilog/parser/verilog_parser.cc:
    --verilog_trace_parser (Trace verilog parser); default: false;


  Flags from verilog/tools/formatter/verilog_format.cc:
    --failsafe_success (If true, always exit with 0 status, even if there were
      input errors or internal errors. In all error conditions, the original
      text is always preserved. This is useful in deploying services where
      fail-safe behaviors should be considered a success.); default: true;
    --format_module_instantiations (If true, format module instantiations (data
      declarations), else leave them unformatted. This is a short-term
      workaround.); default: false;
    --format_module_port_declarations (If true, format module declarations' list
      of port declarations, else leave them unformatted. This is a short-term
      workaround.); default: false;
    --inplace (If true, overwrite the input file on successful conditions.);
      default: false;
    --lines (Specific lines to format, 1-based, comma-separated, inclusive N-M
      ranges, N is short for N-N. By default, left unspecified, all lines are
      enabled for formatting. (repeatable, cumulative)); default: ;
    --max_search_states (Limits the number of search states explored during line
      wrap optimization.); default: 100000;
    --show_equally_optimal_wrappings (If true, print when multiple optimal
      solutions are found (stderr), but continue to operate normally.);
      default: false;
    --show_inter_token_info (If true, along with show_token_partition_tree,
      include inter-token information such as spacing and break penalties.);
      default: false;
    --show_largest_token_partitions (If > 0, print token partitioning and then
      exit without formatting output.); default: 0;
    --show_token_partition_tree (If true, print diagnostics after token
      partitioning and then exit without formatting output.); default: false;
    --stdin_name (When using '-' to read from stdin, this gives an alternate
      name for diagnostic purposes. Otherwise this is ignored.);
      default: "<stdin>";
```

## Version

Generated on 2020-05-06 16:58:51 -0700 from [v0.0-378-g8bfe7a7](https://github.com/google/verible/commit/8bfe7a7f51a238a842d9c8300453f4d2122a963f)