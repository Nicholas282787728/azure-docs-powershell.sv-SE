---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088929"
---
# <span data-ttu-id="1907f-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="1907f-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="1907f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1907f-102">SYNOPSIS</span></span>
<span data-ttu-id="1907f-103">Hämtar smart grupp historik</span><span class="sxs-lookup"><span data-stu-id="1907f-103">Gets smart group history</span></span>

## <span data-ttu-id="1907f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1907f-104">SYNTAX</span></span>

### <span data-ttu-id="1907f-105">BySmartGroupId (standard)</span><span class="sxs-lookup"><span data-stu-id="1907f-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1907f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1907f-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1907f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1907f-107">DESCRIPTION</span></span>
<span data-ttu-id="1907f-108">Cmdleten **Get-AzSmartGroupHistory** -hämtar Smart-grupphistoriken.</span><span class="sxs-lookup"><span data-stu-id="1907f-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="1907f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1907f-109">EXAMPLES</span></span>

### <span data-ttu-id="1907f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1907f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="1907f-111">Hämtar information om smart grupp historik.</span><span class="sxs-lookup"><span data-stu-id="1907f-111">Gets smart group history details.</span></span>

## <span data-ttu-id="1907f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1907f-112">PARAMETERS</span></span>

### <span data-ttu-id="1907f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1907f-113">-DefaultProfile</span></span>
<span data-ttu-id="1907f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1907f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1907f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1907f-115">-InputObject</span></span>
<span data-ttu-id="1907f-116">Indatavärdet från pipeline.</span><span class="sxs-lookup"><span data-stu-id="1907f-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="1907f-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="1907f-117">-SmartGroupId</span></span>
<span data-ttu-id="1907f-118">Unik identifierare för SmartGroup/ResourceId för aviseringen.</span><span class="sxs-lookup"><span data-stu-id="1907f-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="1907f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1907f-119">CommonParameters</span></span>
<span data-ttu-id="1907f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1907f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1907f-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1907f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1907f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1907f-122">INPUTS</span></span>

### <span data-ttu-id="1907f-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="1907f-123">None</span></span>

## <span data-ttu-id="1907f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1907f-124">OUTPUTS</span></span>

### <span data-ttu-id="1907f-125">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="1907f-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="1907f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1907f-126">NOTES</span></span>

## <span data-ttu-id="1907f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1907f-127">RELATED LINKS</span></span>
