---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576078"
---
# <span data-ttu-id="1f729-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="1f729-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="1f729-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f729-102">SYNOPSIS</span></span>
<span data-ttu-id="1f729-103">Uppdaterar ett säkerhets varnings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="1f729-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f729-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f729-104">SYNTAX</span></span>

### <span data-ttu-id="1f729-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="1f729-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f729-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="1f729-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f729-107">ID</span><span class="sxs-lookup"><span data-stu-id="1f729-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f729-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="1f729-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f729-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f729-109">DESCRIPTION</span></span>
<span data-ttu-id="1f729-110">Anger ett säkerhets varnings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="1f729-110">Sets a security alert state.</span></span>

## <span data-ttu-id="1f729-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f729-111">EXAMPLES</span></span>

### <span data-ttu-id="1f729-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f729-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="1f729-113">Avaktiverar en säkerhets varning som har höjts.</span><span class="sxs-lookup"><span data-stu-id="1f729-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="1f729-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f729-114">PARAMETERS</span></span>

### <span data-ttu-id="1f729-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="1f729-115">-ActionType</span></span>
<span data-ttu-id="1f729-116">Åtgärds typ.</span><span class="sxs-lookup"><span data-stu-id="1f729-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f729-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f729-117">-DefaultProfile</span></span>
<span data-ttu-id="1f729-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f729-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f729-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f729-119">-InputObject</span></span>
<span data-ttu-id="1f729-120">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="1f729-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f729-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="1f729-121">-Location</span></span>
<span data-ttu-id="1f729-122">Plats.</span><span class="sxs-lookup"><span data-stu-id="1f729-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f729-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f729-123">-Name</span></span>
<span data-ttu-id="1f729-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1f729-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f729-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f729-125">-PassThru</span></span>
<span data-ttu-id="1f729-126">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="1f729-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="1f729-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f729-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f729-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1f729-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f729-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f729-129">-ResourceId</span></span>
<span data-ttu-id="1f729-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1f729-130">Resource ID.</span></span>

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

### <span data-ttu-id="1f729-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f729-131">-Confirm</span></span>
<span data-ttu-id="1f729-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f729-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f729-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f729-133">-WhatIf</span></span>
<span data-ttu-id="1f729-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f729-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f729-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f729-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f729-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f729-136">CommonParameters</span></span>
<span data-ttu-id="1f729-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f729-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f729-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f729-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f729-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f729-139">INPUTS</span></span>

### <span data-ttu-id="1f729-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1f729-140">System.String</span></span>
<span data-ttu-id="1f729-141">Microsoft. Azure. kommandon. Security. cmdletar. Alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="1f729-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="1f729-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f729-142">OUTPUTS</span></span>

### <span data-ttu-id="1f729-143">Microsoft. Azure. commands. Security. Models. Alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="1f729-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="1f729-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f729-144">NOTES</span></span>

## <span data-ttu-id="1f729-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f729-145">RELATED LINKS</span></span>
