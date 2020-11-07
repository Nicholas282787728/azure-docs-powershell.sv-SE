---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: a9289bc6a0db4403b96e982fd28f91578e3a0c9b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755127"
---
# <span data-ttu-id="d06f2-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d06f2-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="d06f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d06f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d06f2-103">Hämtar nycklarna till ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="d06f2-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="d06f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d06f2-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d06f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d06f2-105">DESCRIPTION</span></span>
<span data-ttu-id="d06f2-106">Cmdleten **Get-AzBatchAccountKey** hämtar nycklarna för ett Azure Batch-konto i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d06f2-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="d06f2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d06f2-107">EXAMPLES</span></span>

### <span data-ttu-id="d06f2-108">Exempel 1: Hämta kommandon för batch-konto och spara det i $Context variabel för användning senare</span><span class="sxs-lookup"><span data-stu-id="d06f2-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="d06f2-109">Det här kommandot får konto informationen och lagrar den i ett `$Context` objekt som ska användas senare.</span><span class="sxs-lookup"><span data-stu-id="d06f2-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="d06f2-110">Exempel 2: Hämta batch-konton och visa dem</span><span class="sxs-lookup"><span data-stu-id="d06f2-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="d06f2-111">Det här kommandot får konto nycklarna och skriver ut dem i konsolen.</span><span class="sxs-lookup"><span data-stu-id="d06f2-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="d06f2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d06f2-112">PARAMETERS</span></span>

### <span data-ttu-id="d06f2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d06f2-113">-AccountName</span></span>
<span data-ttu-id="d06f2-114">Anger namnet på det konto som den här cmdleten hämtar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="d06f2-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06f2-115">-DefaultProfile</span></span>
<span data-ttu-id="d06f2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d06f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d06f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d06f2-118">Anger namnet på den resurs grupp som innehåller det konto som den här cmdleten hämtar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="d06f2-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06f2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06f2-119">CommonParameters</span></span>
<span data-ttu-id="d06f2-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06f2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06f2-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06f2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06f2-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d06f2-122">INPUTS</span></span>

### <span data-ttu-id="d06f2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d06f2-123">System.String</span></span>

## <span data-ttu-id="d06f2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d06f2-124">OUTPUTS</span></span>

### <span data-ttu-id="d06f2-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d06f2-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d06f2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d06f2-126">NOTES</span></span>

## <span data-ttu-id="d06f2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d06f2-127">RELATED LINKS</span></span>

[<span data-ttu-id="d06f2-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d06f2-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="d06f2-129">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d06f2-129">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


