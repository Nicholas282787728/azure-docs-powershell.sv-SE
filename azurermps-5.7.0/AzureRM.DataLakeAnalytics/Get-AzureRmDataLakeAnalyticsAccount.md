---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755610"
---
# <span data-ttu-id="61ad4-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="61ad4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="61ad4-103">Hämtar information om ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="61ad4-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61ad4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61ad4-104">SYNTAX</span></span>

### <span data-ttu-id="61ad4-105">GetAllInSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="61ad4-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61ad4-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61ad4-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61ad4-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61ad4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="61ad4-109">Cmdleten **Get-AzureRmDataLakeAnalyticsAccount** hämtar information om ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="61ad4-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="61ad4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="61ad4-111">Exempel 1: få information om ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="61ad4-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="61ad4-112">Med det här kommandot får du information om kontot ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="61ad4-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="61ad4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61ad4-113">PARAMETERS</span></span>

### <span data-ttu-id="61ad4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ad4-114">-DefaultProfile</span></span>
<span data-ttu-id="61ad4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="61ad4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ad4-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="61ad4-116">-Name</span></span>
<span data-ttu-id="61ad4-117">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="61ad4-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ad4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ad4-118">-ResourceGroupName</span></span>
<span data-ttu-id="61ad4-119">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="61ad4-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ad4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ad4-120">CommonParameters</span></span>
<span data-ttu-id="61ad4-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ad4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ad4-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ad4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ad4-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61ad4-123">INPUTS</span></span>

### <span data-ttu-id="61ad4-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="61ad4-124">None</span></span>
<span data-ttu-id="61ad4-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="61ad4-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61ad4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61ad4-126">OUTPUTS</span></span>

### <span data-ttu-id="61ad4-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="61ad4-128">Angivna konto uppgifter.</span><span class="sxs-lookup"><span data-stu-id="61ad4-128">The specified account details.</span></span>

### <span data-ttu-id="61ad4-129">Förteckning<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="61ad4-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="61ad4-130">Listan med konton i den angivna resurs gruppen eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="61ad4-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="61ad4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61ad4-131">NOTES</span></span>

## <span data-ttu-id="61ad4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61ad4-132">RELATED LINKS</span></span>

[<span data-ttu-id="61ad4-133">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="61ad4-134">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="61ad4-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="61ad4-136">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="61ad4-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


