---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269715"
---
# <span data-ttu-id="dd4e2-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="dd4e2-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="dd4e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4e2-103">Hämtar information om aviserings historik</span><span class="sxs-lookup"><span data-stu-id="dd4e2-103">Gets Alert History information</span></span>

## <span data-ttu-id="dd4e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd4e2-104">SYNTAX</span></span>

### <span data-ttu-id="dd4e2-105">ByAlertId (standard)</span><span class="sxs-lookup"><span data-stu-id="dd4e2-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd4e2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd4e2-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd4e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd4e2-107">DESCRIPTION</span></span>
<span data-ttu-id="dd4e2-108">**Get-AzAlertObjectHistory** cmdlet får historik över aviseringar.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="dd4e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd4e2-109">EXAMPLES</span></span>

### <span data-ttu-id="dd4e2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd4e2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="dd4e2-111">Hämtar information om aviserings historiken.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-111">Gets alert history details.</span></span> 

## <span data-ttu-id="dd4e2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd4e2-112">PARAMETERS</span></span>

### <span data-ttu-id="dd4e2-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="dd4e2-113">-AlertId</span></span>
<span data-ttu-id="dd4e2-114">Unik identifierare för avisering/ResourceId för avisering.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="dd4e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4e2-115">-DefaultProfile</span></span>
<span data-ttu-id="dd4e2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4e2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4e2-117">-InputObject</span></span>
<span data-ttu-id="dd4e2-118">Indatavärdet från pipeline.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="dd4e2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4e2-119">CommonParameters</span></span>
<span data-ttu-id="dd4e2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4e2-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd4e2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4e2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd4e2-122">INPUTS</span></span>

### <span data-ttu-id="dd4e2-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="dd4e2-123">None</span></span>

## <span data-ttu-id="dd4e2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd4e2-124">OUTPUTS</span></span>

### <span data-ttu-id="dd4e2-125">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="dd4e2-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="dd4e2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd4e2-126">NOTES</span></span>

## <span data-ttu-id="dd4e2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd4e2-127">RELATED LINKS</span></span>
