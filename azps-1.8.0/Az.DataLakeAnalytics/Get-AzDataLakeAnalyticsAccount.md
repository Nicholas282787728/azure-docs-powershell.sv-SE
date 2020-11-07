---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b0390f4ec9ec7c141e7d059c88d7aeb4b9c8507d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916990"
---
# <span data-ttu-id="ac18e-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ac18e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac18e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac18e-103">Hämtar information om ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="ac18e-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ac18e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac18e-104">SYNTAX</span></span>

### <span data-ttu-id="ac18e-105">GetAllInSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="ac18e-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac18e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ac18e-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac18e-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac18e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac18e-108">DESCRIPTION</span></span>
<span data-ttu-id="ac18e-109">Cmdleten **Get-AzDataLakeAnalyticsAccount** hämtar information om ett Azure Data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="ac18e-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ac18e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac18e-110">EXAMPLES</span></span>

### <span data-ttu-id="ac18e-111">Exempel 1: få information om ett data Lake Analytics-konto</span><span class="sxs-lookup"><span data-stu-id="ac18e-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="ac18e-112">Med det här kommandot får du information om kontot ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="ac18e-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="ac18e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac18e-113">PARAMETERS</span></span>

### <span data-ttu-id="ac18e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac18e-114">-DefaultProfile</span></span>
<span data-ttu-id="ac18e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ac18e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac18e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac18e-116">-Name</span></span>
<span data-ttu-id="ac18e-117">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ac18e-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac18e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac18e-118">-ResourceGroupName</span></span>
<span data-ttu-id="ac18e-119">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="ac18e-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac18e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac18e-120">CommonParameters</span></span>
<span data-ttu-id="ac18e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac18e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac18e-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac18e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac18e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac18e-123">INPUTS</span></span>

### <span data-ttu-id="ac18e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ac18e-124">System.String</span></span>

## <span data-ttu-id="ac18e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac18e-125">OUTPUTS</span></span>

### <span data-ttu-id="ac18e-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="ac18e-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="ac18e-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="ac18e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac18e-128">NOTES</span></span>

## <span data-ttu-id="ac18e-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac18e-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac18e-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ac18e-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ac18e-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ac18e-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ac18e-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


