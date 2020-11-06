---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583196"
---
# <span data-ttu-id="c3af9-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c3af9-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="c3af9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3af9-102">SYNOPSIS</span></span>
<span data-ttu-id="c3af9-103">Testar förekomsten av ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="c3af9-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3af9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3af9-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3af9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3af9-105">DESCRIPTION</span></span>
<span data-ttu-id="c3af9-106">**Test-AzureRmDataLakeStoreAccount-** cmdleten testar att det finns ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="c3af9-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="c3af9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3af9-107">EXAMPLES</span></span>

### <span data-ttu-id="c3af9-108">Exempel 1: testa ett konto</span><span class="sxs-lookup"><span data-stu-id="c3af9-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c3af9-109">Det här kommandot testar om kontot som heter ContosoADL finns.</span><span class="sxs-lookup"><span data-stu-id="c3af9-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="c3af9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3af9-110">PARAMETERS</span></span>

### <span data-ttu-id="c3af9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3af9-111">-DefaultProfile</span></span>
<span data-ttu-id="c3af9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c3af9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3af9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3af9-113">-Name</span></span>
<span data-ttu-id="c3af9-114">Anger namnet på den data Lake Store-konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="c3af9-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3af9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3af9-115">-ResourceGroupName</span></span>
<span data-ttu-id="c3af9-116">Anger namnet på den resurs grupp som innehåller det konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="c3af9-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3af9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3af9-117">CommonParameters</span></span>
<span data-ttu-id="c3af9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3af9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3af9-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3af9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3af9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3af9-120">INPUTS</span></span>

### <span data-ttu-id="c3af9-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="c3af9-121">None</span></span>
<span data-ttu-id="c3af9-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c3af9-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3af9-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3af9-123">OUTPUTS</span></span>

### <span data-ttu-id="c3af9-124">bool</span><span class="sxs-lookup"><span data-stu-id="c3af9-124">bool</span></span>
<span data-ttu-id="c3af9-125">True eller false anger att det angivna kontot förekommer.</span><span class="sxs-lookup"><span data-stu-id="c3af9-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="c3af9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3af9-126">NOTES</span></span>

## <span data-ttu-id="c3af9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3af9-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3af9-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c3af9-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c3af9-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c3af9-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c3af9-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c3af9-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c3af9-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c3af9-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


