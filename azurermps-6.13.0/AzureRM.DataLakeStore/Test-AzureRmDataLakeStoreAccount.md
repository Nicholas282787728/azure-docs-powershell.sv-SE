---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b1b3a05b6f2d19ba350567c8793822d4129c5445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755202"
---
# <span data-ttu-id="6ebee-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ebee-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="6ebee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ebee-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebee-103">Testar förekomsten av ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6ebee-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ebee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ebee-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ebee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ebee-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebee-106">**Test-AzureRmDataLakeStoreAccount-** cmdleten testar att det finns ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="6ebee-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="6ebee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ebee-107">EXAMPLES</span></span>

### <span data-ttu-id="6ebee-108">Exempel 1: testa ett konto</span><span class="sxs-lookup"><span data-stu-id="6ebee-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="6ebee-109">Det här kommandot testar om kontot som heter ContosoADL finns.</span><span class="sxs-lookup"><span data-stu-id="6ebee-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="6ebee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ebee-110">PARAMETERS</span></span>

### <span data-ttu-id="6ebee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebee-111">-DefaultProfile</span></span>
<span data-ttu-id="6ebee-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6ebee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ebee-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ebee-113">-Name</span></span>
<span data-ttu-id="6ebee-114">Anger namnet på den data Lake Store-konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="6ebee-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="6ebee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebee-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ebee-116">Anger namnet på den resurs grupp som innehåller det konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="6ebee-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="6ebee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebee-117">CommonParameters</span></span>
<span data-ttu-id="6ebee-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ebee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebee-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebee-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ebee-120">INPUTS</span></span>

### <span data-ttu-id="6ebee-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6ebee-121">System.String</span></span>

## <span data-ttu-id="6ebee-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ebee-122">OUTPUTS</span></span>

### <span data-ttu-id="6ebee-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ebee-123">System.Boolean</span></span>

## <span data-ttu-id="6ebee-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ebee-124">NOTES</span></span>

## <span data-ttu-id="6ebee-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ebee-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ebee-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ebee-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6ebee-127">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ebee-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6ebee-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ebee-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="6ebee-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6ebee-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


