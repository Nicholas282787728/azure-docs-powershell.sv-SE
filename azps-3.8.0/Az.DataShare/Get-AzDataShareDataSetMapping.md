---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: cf8b235d0035955f809b167ba4d532cdae0538c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088439"
---
# <span data-ttu-id="3dfc5-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3dfc5-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="3dfc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfc5-103">Hämtar information om data uppsättnings mappningar i dela prenumeration</span><span class="sxs-lookup"><span data-stu-id="3dfc5-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="3dfc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dfc5-104">SYNTAX</span></span>

### <span data-ttu-id="3dfc5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3dfc5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dfc5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfc5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dfc5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dfc5-107">DESCRIPTION</span></span>
<span data-ttu-id="3dfc5-108">Cmdleten **Get-AzDataShareDataSetMapping** hämtar information om en viss data uppsättnings mappning om namnet har angetts.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="3dfc5-109">Annars får du information om alla data uppsättnings mappningar i en resurs prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="3dfc5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dfc5-110">EXAMPLES</span></span>

### <span data-ttu-id="3dfc5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3dfc5-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="3dfc5-112">Det här kommandot visar information om alla data uppsättnings mappningar i Share-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="3dfc5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dfc5-113">PARAMETERS</span></span>

### <span data-ttu-id="3dfc5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3dfc5-114">-AccountName</span></span>
<span data-ttu-id="3dfc5-115">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-115">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfc5-116">-DefaultProfile</span></span>
<span data-ttu-id="3dfc5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dfc5-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3dfc5-118">-Name</span></span>
<span data-ttu-id="3dfc5-119">Mappnings namn för Azure Data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-119">Azure data set mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dfc5-120">-ResourceGroupName</span></span>
<span data-ttu-id="3dfc5-121">Resurs grupp namnet för Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-121">The resource group name of azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dfc5-122">-ResourceId</span></span>
<span data-ttu-id="3dfc5-123">Resurs-ID för Azure Data Set-mappningen.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-123">The resource id of the azure data set mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3dfc5-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="3dfc5-125">Namn på Azure Data Share-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-125">Azure data share subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfc5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfc5-126">CommonParameters</span></span>
<span data-ttu-id="3dfc5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfc5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfc5-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfc5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfc5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dfc5-129">INPUTS</span></span>

### <span data-ttu-id="3dfc5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3dfc5-130">System.String</span></span>

## <span data-ttu-id="3dfc5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dfc5-131">OUTPUTS</span></span>

### <span data-ttu-id="3dfc5-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="3dfc5-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="3dfc5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dfc5-133">NOTES</span></span>

## <span data-ttu-id="3dfc5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dfc5-134">RELATED LINKS</span></span>
