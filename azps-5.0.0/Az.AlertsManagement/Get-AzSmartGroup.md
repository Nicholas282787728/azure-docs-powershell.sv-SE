---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269517"
---
# <span data-ttu-id="a9f26-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="a9f26-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="a9f26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9f26-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f26-103">Hämtar smarta grupp information</span><span class="sxs-lookup"><span data-stu-id="a9f26-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="a9f26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9f26-104">SYNTAX</span></span>

### <span data-ttu-id="a9f26-105">SmartGroupsListByFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="a9f26-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9f26-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="a9f26-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f26-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9f26-107">DESCRIPTION</span></span>
<span data-ttu-id="a9f26-108">Cmdleten **Get-AzSmartGroup** hämtar Smart Group-information.</span><span class="sxs-lookup"><span data-stu-id="a9f26-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="a9f26-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9f26-109">EXAMPLES</span></span>

### <span data-ttu-id="a9f26-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9f26-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="a9f26-111">Lista alla smarta grupper som har skapats under den senaste 1 timmen.</span><span class="sxs-lookup"><span data-stu-id="a9f26-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="a9f26-112">Använd Format-List för att få information om varje smart grupp i listan.</span><span class="sxs-lookup"><span data-stu-id="a9f26-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="a9f26-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a9f26-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="a9f26-114">Få smart grupp information utifrån ID (GUID) eller resurs-ID (fullständigt ARM-ID)</span><span class="sxs-lookup"><span data-stu-id="a9f26-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="a9f26-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9f26-115">PARAMETERS</span></span>

### <span data-ttu-id="a9f26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f26-116">-DefaultProfile</span></span>
<span data-ttu-id="a9f26-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9f26-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f26-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="a9f26-118">-SmartGroupId</span></span>
<span data-ttu-id="a9f26-119">Unik identifierare för SmartGroup/ResourceId för SmartGroup.</span><span class="sxs-lookup"><span data-stu-id="a9f26-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f26-120">-SorteraEfter</span><span class="sxs-lookup"><span data-stu-id="a9f26-120">-SortBy</span></span>
<span data-ttu-id="a9f26-121">Varnings egenskapen som ska användas vid sortering</span><span class="sxs-lookup"><span data-stu-id="a9f26-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f26-122">-Sortering</span><span class="sxs-lookup"><span data-stu-id="a9f26-122">-SortOrder</span></span>
<span data-ttu-id="a9f26-123">Sorterings ordning</span><span class="sxs-lookup"><span data-stu-id="a9f26-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f26-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="a9f26-124">-TimeRange</span></span>
<span data-ttu-id="a9f26-125">Tidsintervalls värden som stöds – 1H, 1d, 7d, 30d (standard är 1d)</span><span class="sxs-lookup"><span data-stu-id="a9f26-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f26-126">CommonParameters</span></span>
<span data-ttu-id="a9f26-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f26-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9f26-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f26-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9f26-129">INPUTS</span></span>

### <span data-ttu-id="a9f26-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="a9f26-130">None</span></span>

## <span data-ttu-id="a9f26-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9f26-131">OUTPUTS</span></span>

### <span data-ttu-id="a9f26-132">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="a9f26-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="a9f26-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9f26-133">NOTES</span></span>

## <span data-ttu-id="a9f26-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9f26-134">RELATED LINKS</span></span>
