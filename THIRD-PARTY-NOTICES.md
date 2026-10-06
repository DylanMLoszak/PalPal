# Third-party notices

PalPal's own licence is in [LICENSE.md](LICENSE.md). It covers PalPal only. The release build also contains the
material listed here, which belongs to its respective owners and is used under its own terms.

## Game data

PalPal ships reference tables describing Palworld (species, passives, breeding combinations, work
suitabilities and similar game facts). Palworld and its game data are the property of Pocketpair, Inc.
The tables were compiled with reference to the community database [paldb.cc](https://paldb.cc) and to the
game's own data files. PalPal claims no rights over this data.

PalPal is an unofficial fan-made tool, not affiliated with, endorsed by or sponsored by Pocketpair, Inc. or
paldb.cc.

## Open-source components

The release build includes the .NET runtime and the following libraries. Each is distributed under the
licence named beside it; the full licence texts are available from the linked projects.

| Component | Licence |
| --- | --- |
| [.NET runtime and WPF](https://github.com/dotnet) | MIT |
| [Blake3](https://www.nuget.org/packages/Blake3) | BSD-2-Clause |
| [BouncyCastle.Cryptography](https://www.nuget.org/packages/BouncyCastle.Cryptography) | MIT |
| [CommunityToolkit.HighPerformance](https://www.nuget.org/packages/CommunityToolkit.HighPerformance) | MIT |
| [CommunityToolkit.Mvvm](https://www.nuget.org/packages/CommunityToolkit.Mvvm) | MIT |
| [CUE4Parse](https://www.nuget.org/packages/CUE4Parse) | Apache-2.0 |
| [FixedMathSharp](https://www.nuget.org/packages/FixedMathSharp) | MIT |
| [Fmod5Sharp](https://www.nuget.org/packages/Fmod5Sharp) | MIT |
| [GenericReader](https://www.nuget.org/packages/GenericReader) | MIT |
| [IndexRange](https://www.nuget.org/packages/IndexRange) | MIT |
| [Infrablack.UE4Config](https://www.nuget.org/packages/Infrablack.UE4Config) | MIT |
| [K4os.Compression.LZ4](https://www.nuget.org/packages/K4os.Compression.LZ4) | MIT |
| [K4os.Compression.LZ4.Streams](https://www.nuget.org/packages/K4os.Compression.LZ4.Streams) | MIT |
| [K4os.Hash.xxHash](https://www.nuget.org/packages/K4os.Hash.xxHash) | MIT |
| [LZMA-SDK](https://www.nuget.org/packages/LZMA-SDK) (SevenZip.dll) | MIT |
| [MemoryPack](https://www.nuget.org/packages/MemoryPack) | MIT |
| [MemoryPack.Core](https://www.nuget.org/packages/MemoryPack.Core) | MIT |
| [Microsoft.Bcl.Memory](https://www.nuget.org/packages/Microsoft.Bcl.Memory) | MIT |
| [NAudio.Core](https://www.nuget.org/packages/NAudio.Core) | MIT |
| [Newtonsoft.Json](https://www.nuget.org/packages/Newtonsoft.Json) | MIT |
| [OffiUtils](https://www.nuget.org/packages/OffiUtils) | MIT |
| [OggVorbisEncoder](https://www.nuget.org/packages/OggVorbisEncoder) | MIT |
| [Oodle.NET](https://www.nuget.org/packages/Oodle.NET) | MIT |
| [OodleSharp](https://www.nuget.org/packages/OodleSharp) | MIT |
| [Serilog](https://www.nuget.org/packages/Serilog) | Apache-2.0 |
| [Serilog.Sinks.Console](https://www.nuget.org/packages/Serilog.Sinks.Console) | Apache-2.0 |
| [SubstreamSharp](https://www.nuget.org/packages/SubstreamSharp) | MIT |
| [System.IO.Hashing](https://www.nuget.org/packages/System.IO.Hashing) | MIT |
| [System.Numerics.Tensors](https://www.nuget.org/packages/System.Numerics.Tensors) | MIT |
| [VGAudio](https://www.nuget.org/packages/VGAudio) | MIT |
| [Zlib-ng.NET](https://www.nuget.org/packages/Zlib-ng.NET) | MIT |
| [ZstdSharp.Port](https://www.nuget.org/packages/ZstdSharp.Port) | MIT |

## Not included, but required

PalPal reads save files through two Python packages that you install yourself and that are not part of the
release: [palworld-save-tools](https://pypi.org/project/palworld-save-tools/) and
[pyooz](https://pypi.org/project/pyooz/).
