---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928198"
---
# <span data-ttu-id="41160-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="41160-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="41160-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41160-102">SYNOPSIS</span></span>
<span data-ttu-id="41160-103">Testar förekomsten av ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="41160-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="41160-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41160-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41160-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41160-105">DESCRIPTION</span></span>
<span data-ttu-id="41160-106">**Test-AzDataLakeStoreAccount-** cmdleten testar att det finns ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="41160-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="41160-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41160-107">EXAMPLES</span></span>

### <span data-ttu-id="41160-108">Exempel 1: testa ett konto</span><span class="sxs-lookup"><span data-stu-id="41160-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="41160-109">Det här kommandot testar om kontot som heter ContosoADL finns.</span><span class="sxs-lookup"><span data-stu-id="41160-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="41160-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41160-110">PARAMETERS</span></span>

### <span data-ttu-id="41160-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41160-111">-DefaultProfile</span></span>
<span data-ttu-id="41160-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="41160-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41160-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="41160-113">-Name</span></span>
<span data-ttu-id="41160-114">Anger namnet på den data Lake Store-konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="41160-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="41160-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41160-115">-ResourceGroupName</span></span>
<span data-ttu-id="41160-116">Anger namnet på den resurs grupp som innehåller det konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="41160-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="41160-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41160-117">CommonParameters</span></span>
<span data-ttu-id="41160-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41160-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41160-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41160-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41160-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41160-120">INPUTS</span></span>

### <span data-ttu-id="41160-121">System. String</span><span class="sxs-lookup"><span data-stu-id="41160-121">System.String</span></span>

## <span data-ttu-id="41160-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41160-122">OUTPUTS</span></span>

### <span data-ttu-id="41160-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41160-123">System.Boolean</span></span>

## <span data-ttu-id="41160-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41160-124">NOTES</span></span>

## <span data-ttu-id="41160-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41160-125">RELATED LINKS</span></span>

[<span data-ttu-id="41160-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="41160-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="41160-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="41160-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="41160-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="41160-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="41160-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="41160-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

