### Usage Examples
- Basic example:
```python
from probing.pipeline import ProbingPipeline

experiment = ProbingPipeline(
        hf_model_name="bert-base-uncased",
        device="cuda:0",
        metric_names=["f1", "accuracy"],
        encoding_batch_size=32,
        classifier_batch_size=32)

experiment.run(probe_task=Path("example.csv").stem,
               path_to_task_file="example.csv",
               verbose=True,
               train_epochs=20,)
```
- For other examples, see [Probing Pipeline documentation](https://github.com/AIRI-Institute/Probing_framework/tree/main/scripts).
