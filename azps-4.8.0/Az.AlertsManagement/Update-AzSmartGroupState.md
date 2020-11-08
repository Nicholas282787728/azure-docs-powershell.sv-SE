---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101254"
---
# <span data-ttu-id="8f22a-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="8f22a-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="8f22a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f22a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f22a-103">Uppdaterar smart grupp status</span><span class="sxs-lookup"><span data-stu-id="8f22a-103">Updates smart group state</span></span>

## <span data-ttu-id="8f22a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f22a-104">SYNTAX</span></span>

### <span data-ttu-id="8f22a-105">BySmartGroupId (standard)</span><span class="sxs-lookup"><span data-stu-id="8f22a-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f22a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f22a-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f22a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f22a-107">DESCRIPTION</span></span>
<span data-ttu-id="8f22a-108">**Update-AzSmartGroupState** cmdlet uppdaterar smart grupp status.</span><span class="sxs-lookup"><span data-stu-id="8f22a-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="8f22a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f22a-109">EXAMPLES</span></span>

### <span data-ttu-id="8f22a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8f22a-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="8f22a-111">Denna cmdlet uppdaterar den smarta gruppen till Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="8f22a-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="8f22a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f22a-112">PARAMETERS</span></span>

### <span data-ttu-id="8f22a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f22a-113">-DefaultProfile</span></span>
<span data-ttu-id="8f22a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f22a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f22a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f22a-115">-InputObject</span></span>
<span data-ttu-id="8f22a-116">Indatavärdet från pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f22a-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f22a-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="8f22a-117">-SmartGroupId</span></span>
<span data-ttu-id="8f22a-118">Unikt ID för smart grupp/ResourceId för smart grupp.</span><span class="sxs-lookup"><span data-stu-id="8f22a-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f22a-119">-State</span><span class="sxs-lookup"><span data-stu-id="8f22a-119">-State</span></span>
<span data-ttu-id="8f22a-120">Uppdaterat läge för smart grupp</span><span class="sxs-lookup"><span data-stu-id="8f22a-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="8f22a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f22a-121">-Confirm</span></span>
<span data-ttu-id="8f22a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f22a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f22a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f22a-123">-WhatIf</span></span>
<span data-ttu-id="8f22a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f22a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f22a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f22a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f22a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f22a-126">CommonParameters</span></span>
<span data-ttu-id="8f22a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f22a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f22a-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f22a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f22a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f22a-129">INPUTS</span></span>

### <span data-ttu-id="8f22a-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="8f22a-130">None</span></span>

## <span data-ttu-id="8f22a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f22a-131">OUTPUTS</span></span>

### <span data-ttu-id="8f22a-132">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="8f22a-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="8f22a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f22a-133">NOTES</span></span>

## <span data-ttu-id="8f22a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f22a-134">RELATED LINKS</span></span>
