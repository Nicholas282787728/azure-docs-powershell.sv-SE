---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420784"
---
# <span data-ttu-id="b3d40-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="b3d40-101">Get-AzDataShare</span></span>

## <span data-ttu-id="b3d40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3d40-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d40-103">Få information om data resurser.</span><span class="sxs-lookup"><span data-stu-id="b3d40-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="b3d40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3d40-104">SYNTAX</span></span>

### <span data-ttu-id="b3d40-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b3d40-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d40-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3d40-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d40-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3d40-107">DESCRIPTION</span></span>
<span data-ttu-id="b3d40-108">Cmdleten **Get-AzDataShare** hämtar information om data resurser i en Azure Data Share-accoount.</span><span class="sxs-lookup"><span data-stu-id="b3d40-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="b3d40-109">Om du anger namnet på en data resurs får denna cmdlet information om den data resursen.</span><span class="sxs-lookup"><span data-stu-id="b3d40-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="b3d40-110">Om du inte anger ett namn hämtas den här cmdleten information om alla data resurser i ett Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="b3d40-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="b3d40-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3d40-111">EXAMPLES</span></span>

### <span data-ttu-id="b3d40-112">Exempel 1: Hämta en specifik data resurs</span><span class="sxs-lookup"><span data-stu-id="b3d40-112">Example 1 : Get a specific data share</span></span>
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

<span data-ttu-id="b3d40-113">Det här kommandot visar information om data AdsShare i Azure Data Share-WikiAdsAccount och resurs grupp annonser.</span><span class="sxs-lookup"><span data-stu-id="b3d40-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="b3d40-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3d40-114">PARAMETERS</span></span>

### <span data-ttu-id="b3d40-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3d40-115">-AccountName</span></span>
<span data-ttu-id="b3d40-116">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="b3d40-116">Azure data share account name</span></span>

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

### <span data-ttu-id="b3d40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d40-117">-DefaultProfile</span></span>
<span data-ttu-id="b3d40-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d40-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d40-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3d40-119">-Name</span></span>
<span data-ttu-id="b3d40-120">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="b3d40-120">Azure data share name</span></span>

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

### <span data-ttu-id="b3d40-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d40-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3d40-122">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="b3d40-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b3d40-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3d40-123">-ResourceId</span></span>
<span data-ttu-id="b3d40-124">Resurs-ID för Azure Data-resursen</span><span class="sxs-lookup"><span data-stu-id="b3d40-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="b3d40-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d40-125">CommonParameters</span></span>
<span data-ttu-id="b3d40-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d40-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d40-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3d40-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d40-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3d40-128">INPUTS</span></span>

### <span data-ttu-id="b3d40-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d40-129">System.String</span></span>

## <span data-ttu-id="b3d40-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3d40-130">OUTPUTS</span></span>

### <span data-ttu-id="b3d40-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="b3d40-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="b3d40-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3d40-132">NOTES</span></span>

## <span data-ttu-id="b3d40-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3d40-133">RELATED LINKS</span></span>
