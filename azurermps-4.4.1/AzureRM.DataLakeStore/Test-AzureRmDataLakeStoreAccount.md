---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585651"
---
# <span data-ttu-id="05185-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05185-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="05185-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05185-102">SYNOPSIS</span></span>
<span data-ttu-id="05185-103">Testar förekomsten av ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="05185-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05185-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05185-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05185-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05185-105">DESCRIPTION</span></span>
<span data-ttu-id="05185-106">**Test-AzureRmDataLakeStoreAccount-** cmdleten testar att det finns ett data Lake Store-konto.</span><span class="sxs-lookup"><span data-stu-id="05185-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="05185-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05185-107">EXAMPLES</span></span>

### <span data-ttu-id="05185-108">Exempel 1: testa ett konto</span><span class="sxs-lookup"><span data-stu-id="05185-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="05185-109">Det här kommandot testar om kontot som heter ContosoADL finns.</span><span class="sxs-lookup"><span data-stu-id="05185-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="05185-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05185-110">PARAMETERS</span></span>

### <span data-ttu-id="05185-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="05185-111">-Name</span></span>
<span data-ttu-id="05185-112">Anger namnet på den data Lake Store-konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="05185-112">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="05185-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05185-113">-ResourceGroupName</span></span>
<span data-ttu-id="05185-114">Anger namnet på den resurs grupp som innehåller det konto som ska testas.</span><span class="sxs-lookup"><span data-stu-id="05185-114">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="05185-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05185-115">-DefaultProfile</span></span>
<span data-ttu-id="05185-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05185-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05185-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05185-117">CommonParameters</span></span>
<span data-ttu-id="05185-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05185-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05185-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05185-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05185-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05185-120">INPUTS</span></span>

## <span data-ttu-id="05185-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05185-121">OUTPUTS</span></span>

### <span data-ttu-id="05185-122">bool</span><span class="sxs-lookup"><span data-stu-id="05185-122">bool</span></span>
<span data-ttu-id="05185-123">True eller false anger att det angivna kontot förekommer.</span><span class="sxs-lookup"><span data-stu-id="05185-123">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="05185-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05185-124">NOTES</span></span>

## <span data-ttu-id="05185-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05185-125">RELATED LINKS</span></span>

[<span data-ttu-id="05185-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05185-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="05185-127">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05185-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="05185-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05185-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="05185-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05185-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


