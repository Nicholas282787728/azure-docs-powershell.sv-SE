---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: e527501424edfbbc12693b47b5858c3c46592402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756191"
---
# <span data-ttu-id="54702-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="54702-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="54702-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54702-102">SYNOPSIS</span></span>
<span data-ttu-id="54702-103">Kontrollerar om det finns ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="54702-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54702-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54702-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54702-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54702-105">DESCRIPTION</span></span>
<span data-ttu-id="54702-106">**Testet AzureRmDataLakeAnalyticsAccount** söker efter ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="54702-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="54702-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54702-107">EXAMPLES</span></span>

### <span data-ttu-id="54702-108">Exempel 1: testa om ett konto finns</span><span class="sxs-lookup"><span data-stu-id="54702-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="54702-109">Det här kommandot testar om kontot som heter ContosoAdlAccount finns.</span><span class="sxs-lookup"><span data-stu-id="54702-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="54702-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54702-110">PARAMETERS</span></span>

### <span data-ttu-id="54702-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54702-111">-DefaultProfile</span></span>
<span data-ttu-id="54702-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="54702-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54702-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="54702-113">-Name</span></span>
<span data-ttu-id="54702-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="54702-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54702-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54702-115">-ResourceGroupName</span></span>
<span data-ttu-id="54702-116">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="54702-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54702-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54702-117">CommonParameters</span></span>
<span data-ttu-id="54702-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54702-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54702-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54702-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54702-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54702-120">INPUTS</span></span>

### <span data-ttu-id="54702-121">System. String</span><span class="sxs-lookup"><span data-stu-id="54702-121">System.String</span></span>

## <span data-ttu-id="54702-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54702-122">OUTPUTS</span></span>

### <span data-ttu-id="54702-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54702-123">System.Boolean</span></span>

## <span data-ttu-id="54702-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54702-124">NOTES</span></span>

## <span data-ttu-id="54702-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54702-125">RELATED LINKS</span></span>

[<span data-ttu-id="54702-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="54702-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="54702-127">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="54702-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="54702-128">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="54702-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


