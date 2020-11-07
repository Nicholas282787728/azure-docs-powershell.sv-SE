---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755454"
---
# <span data-ttu-id="06b44-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="06b44-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="06b44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06b44-102">SYNOPSIS</span></span>
<span data-ttu-id="06b44-103">Hämtar information om ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="06b44-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06b44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06b44-104">SYNTAX</span></span>

### <span data-ttu-id="06b44-105">Allt i abonnemanget (standard)</span><span class="sxs-lookup"><span data-stu-id="06b44-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06b44-106">Alla i resurs grupp</span><span class="sxs-lookup"><span data-stu-id="06b44-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06b44-107">Specifikt konto</span><span class="sxs-lookup"><span data-stu-id="06b44-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06b44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06b44-108">DESCRIPTION</span></span>
<span data-ttu-id="06b44-109">Cmdleten **Get-AzureRmDataLakeAnalyticsAccount** hämtar information om ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="06b44-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="06b44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06b44-110">EXAMPLES</span></span>

### <span data-ttu-id="06b44-111">Exempel 1: få information om ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="06b44-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="06b44-112">Med det här kommandot får du information om kontot ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="06b44-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="06b44-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06b44-113">PARAMETERS</span></span>

### <span data-ttu-id="06b44-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="06b44-114">-Name</span></span>
<span data-ttu-id="06b44-115">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="06b44-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b44-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b44-116">-ResourceGroupName</span></span>
<span data-ttu-id="06b44-117">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="06b44-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06b44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b44-118">-DefaultProfile</span></span>
<span data-ttu-id="06b44-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06b44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b44-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b44-120">CommonParameters</span></span>
<span data-ttu-id="06b44-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b44-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b44-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b44-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b44-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06b44-123">INPUTS</span></span>

## <span data-ttu-id="06b44-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06b44-124">OUTPUTS</span></span>

### <span data-ttu-id="06b44-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="06b44-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="06b44-126">Angivna konto uppgifter.</span><span class="sxs-lookup"><span data-stu-id="06b44-126">The specified account details.</span></span>

### <span data-ttu-id="06b44-127">Förteckning<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="06b44-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="06b44-128">Listan med konton i den angivna resurs gruppen eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="06b44-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="06b44-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06b44-129">NOTES</span></span>

## <span data-ttu-id="06b44-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06b44-130">RELATED LINKS</span></span>

[<span data-ttu-id="06b44-131">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="06b44-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="06b44-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="06b44-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="06b44-133">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="06b44-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="06b44-134">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="06b44-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


