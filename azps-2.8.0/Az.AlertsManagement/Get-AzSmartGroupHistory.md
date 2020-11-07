---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7ed232d14d215966b6cfad3ba788d3c80938316c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745915"
---
# <span data-ttu-id="b665a-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="b665a-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="b665a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b665a-102">SYNOPSIS</span></span>
<span data-ttu-id="b665a-103">Hämtar smart grupp historik</span><span class="sxs-lookup"><span data-stu-id="b665a-103">Gets smart group history</span></span>

## <span data-ttu-id="b665a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b665a-104">SYNTAX</span></span>

### <span data-ttu-id="b665a-105">BySmartGroupId (standard)</span><span class="sxs-lookup"><span data-stu-id="b665a-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b665a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b665a-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b665a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b665a-107">DESCRIPTION</span></span>
<span data-ttu-id="b665a-108">Cmdleten **Get-AzSmartGroupHistory** -hämtar Smart-grupphistoriken.</span><span class="sxs-lookup"><span data-stu-id="b665a-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="b665a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b665a-109">EXAMPLES</span></span>

### <span data-ttu-id="b665a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b665a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="b665a-111">Hämtar information om smart grupp historik.</span><span class="sxs-lookup"><span data-stu-id="b665a-111">Gets smart group history details.</span></span>

## <span data-ttu-id="b665a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b665a-112">PARAMETERS</span></span>

### <span data-ttu-id="b665a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b665a-113">-DefaultProfile</span></span>
<span data-ttu-id="b665a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b665a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b665a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b665a-115">-InputObject</span></span>
<span data-ttu-id="b665a-116">Indatavärdet från pipeline.</span><span class="sxs-lookup"><span data-stu-id="b665a-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="b665a-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="b665a-117">-SmartGroupId</span></span>
<span data-ttu-id="b665a-118">Unik identifierare för SmartGroup/ResourceId för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="b665a-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="b665a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b665a-119">CommonParameters</span></span>
<span data-ttu-id="b665a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b665a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b665a-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b665a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b665a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b665a-122">INPUTS</span></span>

### <span data-ttu-id="b665a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="b665a-123">None</span></span>

## <span data-ttu-id="b665a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b665a-124">OUTPUTS</span></span>

### <span data-ttu-id="b665a-125">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="b665a-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="b665a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b665a-126">NOTES</span></span>

## <span data-ttu-id="b665a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b665a-127">RELATED LINKS</span></span>