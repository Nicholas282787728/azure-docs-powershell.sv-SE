---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525628"
---
# <span data-ttu-id="8c2be-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8c2be-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8c2be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c2be-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2be-103">Tar bort en princip för en JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="8c2be-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="8c2be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c2be-104">SYNTAX</span></span>

### <span data-ttu-id="8c2be-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="8c2be-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c2be-106">ID</span><span class="sxs-lookup"><span data-stu-id="8c2be-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c2be-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8c2be-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c2be-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c2be-108">DESCRIPTION</span></span>
<span data-ttu-id="8c2be-109">Tar bort en princip för nätverks åtkomst i tid.</span><span class="sxs-lookup"><span data-stu-id="8c2be-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="8c2be-110">Efter den här åtgärden kan användaren inte begära tillfälliga nätverks anslutningar på de virtuella datorerna som har kon figurer ATS i den borttagna principen.</span><span class="sxs-lookup"><span data-stu-id="8c2be-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="8c2be-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c2be-111">EXAMPLES</span></span>

### <span data-ttu-id="8c2be-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c2be-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="8c2be-113">Tar bort en princip för nätverks åtkomst i tid.</span><span class="sxs-lookup"><span data-stu-id="8c2be-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="8c2be-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c2be-114">PARAMETERS</span></span>

### <span data-ttu-id="8c2be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2be-115">-DefaultProfile</span></span>
<span data-ttu-id="8c2be-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c2be-117">-InputObject</span></span>
<span data-ttu-id="8c2be-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="8c2be-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="8c2be-119">-Location</span></span>
<span data-ttu-id="8c2be-120">Plats.</span><span class="sxs-lookup"><span data-stu-id="8c2be-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c2be-121">-Name</span></span>
<span data-ttu-id="8c2be-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="8c2be-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c2be-123">-PassThru</span></span>
<span data-ttu-id="8c2be-124">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="8c2be-124">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c2be-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c2be-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8c2be-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c2be-127">-ResourceId</span></span>
<span data-ttu-id="8c2be-128">Resurs-ID för resursen för JIT-nätverksanslutning.</span><span class="sxs-lookup"><span data-stu-id="8c2be-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c2be-129">-Confirm</span></span>
<span data-ttu-id="8c2be-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c2be-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c2be-131">-WhatIf</span></span>
<span data-ttu-id="8c2be-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c2be-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c2be-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c2be-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2be-134">CommonParameters</span></span>
<span data-ttu-id="8c2be-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2be-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c2be-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2be-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c2be-137">INPUTS</span></span>

### <span data-ttu-id="8c2be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8c2be-138">System.String</span></span>

### <span data-ttu-id="8c2be-139">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8c2be-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="8c2be-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c2be-140">OUTPUTS</span></span>

### <span data-ttu-id="8c2be-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c2be-141">System.Boolean</span></span>

## <span data-ttu-id="8c2be-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c2be-142">NOTES</span></span>

## <span data-ttu-id="8c2be-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c2be-143">RELATED LINKS</span></span>
