if (!localPlayer)
                    continue;

                const auto localPlayerTeam = mem.Read<std::uintptr_t>(localPlayer + offsets::teamNum);
                const auto localPlayerFlags = mem.Read<std::uintptr_t>(localPlayer + offsets::flags);

                // bhop
                if (GetAsyncKeyState(VK_SPACE))
                    (localPlayerFlags & (1 << 0)) ?
                    mem.Write<std::uintptr_t>(client + offsets::forceJump, 6) :
                    mem.Write<std::uintptr_t>(client + offsets::forceJump, 4);
