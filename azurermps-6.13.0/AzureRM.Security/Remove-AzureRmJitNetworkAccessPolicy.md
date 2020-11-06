---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576082"
---
# <span data-ttu-id="45559-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="45559-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="45559-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45559-102">SYNOPSIS</span></span>
<span data-ttu-id="45559-103">Tar bort en princip för en JIT-nätverks åtkomst.</span><span class="sxs-lookup"><span data-stu-id="45559-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45559-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45559-104">SYNTAX</span></span>

### <span data-ttu-id="45559-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="45559-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45559-106">ID</span><span class="sxs-lookup"><span data-stu-id="45559-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45559-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="45559-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45559-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45559-108">DESCRIPTION</span></span>
<span data-ttu-id="45559-109">Tar bort en princip för nätverks åtkomst i tid.</span><span class="sxs-lookup"><span data-stu-id="45559-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="45559-110">Efter den här åtgärden kan användaren inte begära tillfälliga nätverks anslutningar på de virtuella datorerna som har kon figurer ATS i den borttagna principen.</span><span class="sxs-lookup"><span data-stu-id="45559-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="45559-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45559-111">EXAMPLES</span></span>

### <span data-ttu-id="45559-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="45559-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="45559-113">Tar bort en princip för nätverks åtkomst i tid.</span><span class="sxs-lookup"><span data-stu-id="45559-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="45559-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45559-114">PARAMETERS</span></span>

### <span data-ttu-id="45559-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45559-115">-DefaultProfile</span></span>
<span data-ttu-id="45559-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45559-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45559-117">-InputObject</span></span>
<span data-ttu-id="45559-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="45559-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45559-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="45559-119">-Location</span></span>
<span data-ttu-id="45559-120">Plats.</span><span class="sxs-lookup"><span data-stu-id="45559-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="45559-121">-Name</span></span>
<span data-ttu-id="45559-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="45559-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45559-123">-PassThru</span></span>
<span data-ttu-id="45559-124">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="45559-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45559-125">-ResourceGroupName</span></span>
<span data-ttu-id="45559-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="45559-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45559-127">-ResourceId</span></span>
<span data-ttu-id="45559-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="45559-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45559-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45559-129">-Confirm</span></span>
<span data-ttu-id="45559-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45559-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45559-131">-WhatIf</span></span>
<span data-ttu-id="45559-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45559-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45559-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45559-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45559-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45559-134">CommonParameters</span></span>
<span data-ttu-id="45559-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45559-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45559-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45559-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45559-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45559-137">INPUTS</span></span>

### <span data-ttu-id="45559-138">System. String</span><span class="sxs-lookup"><span data-stu-id="45559-138">System.String</span></span>
<span data-ttu-id="45559-139">Microsoft. Azure. kommandon. Security. cmdletar. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="45559-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="45559-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45559-140">OUTPUTS</span></span>

### <span data-ttu-id="45559-141">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="45559-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="45559-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45559-142">NOTES</span></span>

## <span data-ttu-id="45559-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45559-143">RELATED LINKS</span></span>
