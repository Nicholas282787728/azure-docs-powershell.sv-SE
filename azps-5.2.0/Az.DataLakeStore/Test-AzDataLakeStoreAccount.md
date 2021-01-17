---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418099"
---
# <span data-ttu-id="accf5-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="accf5-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="accf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="accf5-102">SYNOPSIS</span></span>
<span data-ttu-id="accf5-103">Testar förekomsten av ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="accf5-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="accf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="accf5-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="accf5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="accf5-105">DESCRIPTION</span></span>
<span data-ttu-id="accf5-106">**Test-AzDataLakeStoreAccount-** cmdleten testar att det finns ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="accf5-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="accf5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="accf5-107">EXAMPLES</span></span>

### <span data-ttu-id="accf5-108">Exempel 1: testa ett konto</span><span class="sxs-lookup"><span data-stu-id="accf5-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="accf5-109">Det här kommandot testar om kontot som heter ContosoADL finns.</span><span class="sxs-lookup"><span data-stu-id="accf5-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="accf5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="accf5-110">PARAMETERS</span></span>

### <span data-ttu-id="accf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="accf5-111">-DefaultProfile</span></span>
<span data-ttu-id="accf5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="accf5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="accf5-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="accf5-113">-Name</span></span>
<span data-ttu-id="accf5-114">Anger namnet på den data Lake Store-konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="accf5-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="accf5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="accf5-115">-ResourceGroupName</span></span>
<span data-ttu-id="accf5-116">Anger namnet på den resurs grupp som innehåller det konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="accf5-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="accf5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="accf5-117">CommonParameters</span></span>
<span data-ttu-id="accf5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="accf5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="accf5-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="accf5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="accf5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="accf5-120">INPUTS</span></span>

### <span data-ttu-id="accf5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="accf5-121">System.String</span></span>

## <span data-ttu-id="accf5-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="accf5-122">OUTPUTS</span></span>

### <span data-ttu-id="accf5-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="accf5-123">System.Boolean</span></span>

## <span data-ttu-id="accf5-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="accf5-124">NOTES</span></span>

## <span data-ttu-id="accf5-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="accf5-125">RELATED LINKS</span></span>

[<span data-ttu-id="accf5-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="accf5-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="accf5-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="accf5-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="accf5-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="accf5-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="accf5-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="accf5-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


