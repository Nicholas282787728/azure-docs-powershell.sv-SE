---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744609"
---
# <span data-ttu-id="cff48-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cff48-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="cff48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cff48-102">SYNOPSIS</span></span>
<span data-ttu-id="cff48-103">Kontrollerar om det finns ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="cff48-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="cff48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cff48-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff48-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cff48-105">DESCRIPTION</span></span>
<span data-ttu-id="cff48-106">**Testet AzDataLakeAnalyticsAccount** söker efter ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="cff48-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="cff48-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cff48-107">EXAMPLES</span></span>

### <span data-ttu-id="cff48-108">Exempel 1: testa om ett konto finns</span><span class="sxs-lookup"><span data-stu-id="cff48-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="cff48-109">Det här kommandot testar om kontot som heter ContosoAdlAccount finns.</span><span class="sxs-lookup"><span data-stu-id="cff48-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="cff48-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cff48-110">PARAMETERS</span></span>

### <span data-ttu-id="cff48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff48-111">-DefaultProfile</span></span>
<span data-ttu-id="cff48-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cff48-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cff48-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cff48-113">-Name</span></span>
<span data-ttu-id="cff48-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="cff48-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cff48-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff48-115">-ResourceGroupName</span></span>
<span data-ttu-id="cff48-116">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="cff48-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="cff48-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff48-117">CommonParameters</span></span>
<span data-ttu-id="cff48-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff48-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff48-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff48-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff48-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cff48-120">INPUTS</span></span>

### <span data-ttu-id="cff48-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cff48-121">System.String</span></span>

## <span data-ttu-id="cff48-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cff48-122">OUTPUTS</span></span>

### <span data-ttu-id="cff48-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cff48-123">System.Boolean</span></span>

## <span data-ttu-id="cff48-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cff48-124">NOTES</span></span>

## <span data-ttu-id="cff48-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cff48-125">RELATED LINKS</span></span>

[<span data-ttu-id="cff48-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cff48-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="cff48-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cff48-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="cff48-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cff48-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

