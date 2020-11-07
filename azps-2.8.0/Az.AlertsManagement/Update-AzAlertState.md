---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: faa968803c91b9713482e6930933c49577dab643
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745901"
---
# <span data-ttu-id="55e60-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="55e60-101">Update-AzAlertState</span></span>

## <span data-ttu-id="55e60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55e60-102">SYNOPSIS</span></span>
<span data-ttu-id="55e60-103">Uppdaterar aviserings tillståndet</span><span class="sxs-lookup"><span data-stu-id="55e60-103">Updates alert state</span></span>

## <span data-ttu-id="55e60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55e60-104">SYNTAX</span></span>

### <span data-ttu-id="55e60-105">ByAlertId (standard)</span><span class="sxs-lookup"><span data-stu-id="55e60-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55e60-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="55e60-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55e60-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55e60-107">DESCRIPTION</span></span>
<span data-ttu-id="55e60-108">**Update-AzAlertState** cmdlet uppdaterar aviserings tillståndet.</span><span class="sxs-lookup"><span data-stu-id="55e60-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="55e60-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55e60-109">EXAMPLES</span></span>

### <span data-ttu-id="55e60-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="55e60-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="55e60-111">Denna cmdlet uppdaterar aviserings tillståndet till stängt.</span><span class="sxs-lookup"><span data-stu-id="55e60-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="55e60-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55e60-112">PARAMETERS</span></span>

### <span data-ttu-id="55e60-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="55e60-113">-AlertId</span></span>
<span data-ttu-id="55e60-114">Unik identifierare för avisering/ResourceId för avisering.</span><span class="sxs-lookup"><span data-stu-id="55e60-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e60-115">-DefaultProfile</span></span>
<span data-ttu-id="55e60-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55e60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55e60-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55e60-117">-InputObject</span></span>
<span data-ttu-id="55e60-118">Indatavärdet från pipeline.</span><span class="sxs-lookup"><span data-stu-id="55e60-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55e60-119">-State</span><span class="sxs-lookup"><span data-stu-id="55e60-119">-State</span></span>
<span data-ttu-id="55e60-120">Uppdaterat varnings tillstånd</span><span class="sxs-lookup"><span data-stu-id="55e60-120">Updated Alert State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e60-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55e60-121">-Confirm</span></span>
<span data-ttu-id="55e60-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55e60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e60-123">-WhatIf</span></span>
<span data-ttu-id="55e60-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55e60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55e60-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55e60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55e60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e60-126">CommonParameters</span></span>
<span data-ttu-id="55e60-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e60-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55e60-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e60-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55e60-129">INPUTS</span></span>

### <span data-ttu-id="55e60-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="55e60-130">None</span></span>

## <span data-ttu-id="55e60-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55e60-131">OUTPUTS</span></span>

### <span data-ttu-id="55e60-132">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="55e60-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="55e60-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55e60-133">NOTES</span></span>

## <span data-ttu-id="55e60-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55e60-134">RELATED LINKS</span></span>
