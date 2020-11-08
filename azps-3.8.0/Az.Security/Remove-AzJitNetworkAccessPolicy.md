---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 21a31d2d4e094e986ad862bfe69baef98148e5f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089313"
---
# <span data-ttu-id="a8940-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8940-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a8940-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8940-102">SYNOPSIS</span></span>
<span data-ttu-id="a8940-103">Tar bort en princip för en JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="a8940-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="a8940-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8940-104">SYNTAX</span></span>

### <span data-ttu-id="a8940-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a8940-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8940-106">ID</span><span class="sxs-lookup"><span data-stu-id="a8940-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8940-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8940-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8940-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8940-108">DESCRIPTION</span></span>
<span data-ttu-id="a8940-109">Tar bort en princip för nätverks åtkomst i tid.</span><span class="sxs-lookup"><span data-stu-id="a8940-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="a8940-110">Efter den här åtgärden kan användaren inte begära tillfälliga nätverks anslutningar på de virtuella datorerna som har kon figurer ATS i den borttagna principen.</span><span class="sxs-lookup"><span data-stu-id="a8940-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="a8940-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8940-111">EXAMPLES</span></span>

### <span data-ttu-id="a8940-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8940-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="a8940-113">Tar bort en princip för nätverks åtkomst i tid.</span><span class="sxs-lookup"><span data-stu-id="a8940-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="a8940-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8940-114">PARAMETERS</span></span>

### <span data-ttu-id="a8940-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8940-115">-DefaultProfile</span></span>
<span data-ttu-id="a8940-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8940-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8940-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8940-117">-InputObject</span></span>
<span data-ttu-id="a8940-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="a8940-118">Input Object.</span></span>

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

### <span data-ttu-id="a8940-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="a8940-119">-Location</span></span>
<span data-ttu-id="a8940-120">Plats.</span><span class="sxs-lookup"><span data-stu-id="a8940-120">Location.</span></span>

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

### <span data-ttu-id="a8940-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8940-121">-Name</span></span>
<span data-ttu-id="a8940-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a8940-122">Resource name.</span></span>

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

### <span data-ttu-id="a8940-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8940-123">-PassThru</span></span>
<span data-ttu-id="a8940-124">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="a8940-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a8940-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8940-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8940-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a8940-126">Resource group name.</span></span>

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

### <span data-ttu-id="a8940-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8940-127">-ResourceId</span></span>
<span data-ttu-id="a8940-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a8940-128">Resource ID.</span></span>

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

### <span data-ttu-id="a8940-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8940-129">-Confirm</span></span>
<span data-ttu-id="a8940-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8940-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8940-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8940-131">-WhatIf</span></span>
<span data-ttu-id="a8940-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8940-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8940-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8940-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8940-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8940-134">CommonParameters</span></span>
<span data-ttu-id="a8940-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8940-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8940-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8940-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8940-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8940-137">INPUTS</span></span>

### <span data-ttu-id="a8940-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8940-138">System.String</span></span>

### <span data-ttu-id="a8940-139">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8940-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a8940-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8940-140">OUTPUTS</span></span>

### <span data-ttu-id="a8940-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8940-141">System.Boolean</span></span>

## <span data-ttu-id="a8940-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8940-142">NOTES</span></span>

## <span data-ttu-id="a8940-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8940-143">RELATED LINKS</span></span>
