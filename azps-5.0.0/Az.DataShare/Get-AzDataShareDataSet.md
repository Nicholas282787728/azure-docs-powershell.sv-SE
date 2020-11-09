---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320364"
---
# <span data-ttu-id="c842f-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="c842f-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="c842f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c842f-102">SYNOPSIS</span></span>
<span data-ttu-id="c842f-103">Hämtar information om data uppsättningar i Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="c842f-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="c842f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c842f-104">SYNTAX</span></span>

### <span data-ttu-id="c842f-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c842f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c842f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c842f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c842f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c842f-107">DESCRIPTION</span></span>
<span data-ttu-id="c842f-108">Cmdleten **Get-AzDataShareDataSet** hämtar information om data uppsättningar som lagts till i en resurs i ett Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="c842f-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="c842f-109">Om du anger namnet på data uppsättningen får denna cmdlet information om data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="c842f-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="c842f-110">Om du inte anger ett namn hämtas den här cmdleten information om alla data uppsättningar i en resurs. I</span><span class="sxs-lookup"><span data-stu-id="c842f-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="c842f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c842f-111">EXAMPLES</span></span>

### <span data-ttu-id="c842f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c842f-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="c842f-113">Det här kommandot visar information om data set AdsDataSet i dela AdsShare i Azure Data Share-konto WikiAdsAccount och resurs grupp annonser.</span><span class="sxs-lookup"><span data-stu-id="c842f-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="c842f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c842f-114">PARAMETERS</span></span>

### <span data-ttu-id="c842f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c842f-115">-AccountName</span></span>
<span data-ttu-id="c842f-116">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="c842f-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="c842f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c842f-117">-DefaultProfile</span></span>
<span data-ttu-id="c842f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c842f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c842f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c842f-119">-Name</span></span>
<span data-ttu-id="c842f-120">Namn på Azure Data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="c842f-120">Azure data set name.</span></span>

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

### <span data-ttu-id="c842f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c842f-121">-ResourceGroupName</span></span>
<span data-ttu-id="c842f-122">Resurs grupp namnet för Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="c842f-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="c842f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c842f-123">-ResourceId</span></span>
<span data-ttu-id="c842f-124">Resurs-ID för Azure-datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="c842f-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="c842f-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c842f-125">-ShareName</span></span>
<span data-ttu-id="c842f-126">Azure Data Share-namn.</span><span class="sxs-lookup"><span data-stu-id="c842f-126">Azure data share name.</span></span>

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

### <span data-ttu-id="c842f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c842f-127">CommonParameters</span></span>
<span data-ttu-id="c842f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c842f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c842f-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c842f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c842f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c842f-130">INPUTS</span></span>

### <span data-ttu-id="c842f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c842f-131">System.String</span></span>

## <span data-ttu-id="c842f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c842f-132">OUTPUTS</span></span>

### <span data-ttu-id="c842f-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="c842f-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="c842f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c842f-134">NOTES</span></span>

## <span data-ttu-id="c842f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c842f-135">RELATED LINKS</span></span>
