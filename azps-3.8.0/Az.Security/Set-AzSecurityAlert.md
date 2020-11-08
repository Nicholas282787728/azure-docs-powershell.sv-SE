---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 9618720b234f00700100e14b4e973e3a57f22705
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091501"
---
# <span data-ttu-id="9b85a-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="9b85a-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="9b85a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b85a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b85a-103">Uppdaterar ett säkerhets varnings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="9b85a-103">Updates a security alert state.</span></span>

## <span data-ttu-id="9b85a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b85a-104">SYNTAX</span></span>

### <span data-ttu-id="9b85a-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="9b85a-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b85a-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="9b85a-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b85a-107">ID</span><span class="sxs-lookup"><span data-stu-id="9b85a-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b85a-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="9b85a-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b85a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b85a-109">DESCRIPTION</span></span>
<span data-ttu-id="9b85a-110">Anger ett säkerhets varnings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="9b85a-110">Sets a security alert state.</span></span>

## <span data-ttu-id="9b85a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b85a-111">EXAMPLES</span></span>

### <span data-ttu-id="9b85a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b85a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="9b85a-113">Avaktiverar en säkerhets varning som har höjts.</span><span class="sxs-lookup"><span data-stu-id="9b85a-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="9b85a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b85a-114">PARAMETERS</span></span>

### <span data-ttu-id="9b85a-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="9b85a-115">-ActionType</span></span>
<span data-ttu-id="9b85a-116">Åtgärds typ.</span><span class="sxs-lookup"><span data-stu-id="9b85a-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b85a-117">-DefaultProfile</span></span>
<span data-ttu-id="9b85a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b85a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b85a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b85a-119">-InputObject</span></span>
<span data-ttu-id="9b85a-120">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="9b85a-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="9b85a-121">-Location</span></span>
<span data-ttu-id="9b85a-122">Plats.</span><span class="sxs-lookup"><span data-stu-id="9b85a-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9b85a-123">-Name</span></span>
<span data-ttu-id="9b85a-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9b85a-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b85a-125">-PassThru</span></span>
<span data-ttu-id="9b85a-126">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="9b85a-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9b85a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b85a-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b85a-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9b85a-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b85a-129">-ResourceId</span></span>
<span data-ttu-id="9b85a-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9b85a-130">Resource ID.</span></span>

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

### <span data-ttu-id="9b85a-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b85a-131">-Confirm</span></span>
<span data-ttu-id="9b85a-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b85a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b85a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b85a-133">-WhatIf</span></span>
<span data-ttu-id="9b85a-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b85a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b85a-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b85a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b85a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b85a-136">CommonParameters</span></span>
<span data-ttu-id="9b85a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b85a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b85a-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b85a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b85a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b85a-139">INPUTS</span></span>

### <span data-ttu-id="9b85a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9b85a-140">System.String</span></span>

### <span data-ttu-id="9b85a-141">Microsoft. Azure. commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="9b85a-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="9b85a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b85a-142">OUTPUTS</span></span>

### <span data-ttu-id="9b85a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b85a-143">System.Boolean</span></span>

## <span data-ttu-id="9b85a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b85a-144">NOTES</span></span>

## <span data-ttu-id="9b85a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b85a-145">RELATED LINKS</span></span>
