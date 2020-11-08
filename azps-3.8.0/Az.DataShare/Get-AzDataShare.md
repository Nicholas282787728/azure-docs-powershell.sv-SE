---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a01d67a5ebf98e07a9410903e4c00b4ed4ee70a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088690"
---
# <span data-ttu-id="10dc4-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="10dc4-101">Get-AzDataShare</span></span>

## <span data-ttu-id="10dc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="10dc4-103">Få information om data resurser.</span><span class="sxs-lookup"><span data-stu-id="10dc4-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="10dc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10dc4-104">SYNTAX</span></span>

### <span data-ttu-id="10dc4-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="10dc4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10dc4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10dc4-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10dc4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="10dc4-108">Cmdleten **Get-AzDataShare** hämtar information om data resurser i en Azure Data Share-accoount.</span><span class="sxs-lookup"><span data-stu-id="10dc4-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="10dc4-109">Om du anger namnet på en data resurs får denna cmdlet information om den data resursen.</span><span class="sxs-lookup"><span data-stu-id="10dc4-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="10dc4-110">Om du inte anger ett namn hämtas den här cmdleten information om alla data resurser i ett Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="10dc4-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="10dc4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10dc4-111">EXAMPLES</span></span>

### <span data-ttu-id="10dc4-112">Exempel 1: Hämta en specifik data resurs</span><span class="sxs-lookup"><span data-stu-id="10dc4-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="10dc4-113">Det här kommandot visar information om data AdsShare i Azure Data Share-WikiAdsAccount och resurs grupp annonser.</span><span class="sxs-lookup"><span data-stu-id="10dc4-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="10dc4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10dc4-114">PARAMETERS</span></span>

### <span data-ttu-id="10dc4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10dc4-115">-AccountName</span></span>
<span data-ttu-id="10dc4-116">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="10dc4-116">Azure data share account name</span></span>

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

### <span data-ttu-id="10dc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10dc4-117">-DefaultProfile</span></span>
<span data-ttu-id="10dc4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10dc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10dc4-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="10dc4-119">-Name</span></span>
<span data-ttu-id="10dc4-120">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="10dc4-120">Azure data share name</span></span>

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

### <span data-ttu-id="10dc4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10dc4-121">-ResourceGroupName</span></span>
<span data-ttu-id="10dc4-122">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="10dc4-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="10dc4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10dc4-123">-ResourceId</span></span>
<span data-ttu-id="10dc4-124">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="10dc4-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="10dc4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10dc4-125">CommonParameters</span></span>
<span data-ttu-id="10dc4-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10dc4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10dc4-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10dc4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10dc4-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10dc4-128">INPUTS</span></span>

### <span data-ttu-id="10dc4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="10dc4-129">System.String</span></span>

## <span data-ttu-id="10dc4-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10dc4-130">OUTPUTS</span></span>

### <span data-ttu-id="10dc4-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="10dc4-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="10dc4-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10dc4-132">NOTES</span></span>

## <span data-ttu-id="10dc4-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10dc4-133">RELATED LINKS</span></span>