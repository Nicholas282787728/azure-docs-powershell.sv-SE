---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757312"
---
# <span data-ttu-id="dbf3b-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dbf3b-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="dbf3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbf3b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf3b-103">Hämtar nycklarna till ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbf3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbf3b-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbf3b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbf3b-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf3b-106">Cmdleten **Get-AzureRmBatchAccountKeys** hämtar nycklarna för ett Azure Batch-konto i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="dbf3b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbf3b-107">EXAMPLES</span></span>

## <span data-ttu-id="dbf3b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbf3b-108">PARAMETERS</span></span>

### <span data-ttu-id="dbf3b-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dbf3b-109">-AccountName</span></span>
<span data-ttu-id="dbf3b-110">Anger namnet på det konto som den här cmdleten hämtar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="dbf3b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf3b-111">-ResourceGroupName</span></span>
<span data-ttu-id="dbf3b-112">Anger namnet på den resurs grupp som innehåller det konto som den här cmdleten hämtar nycklar för.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="dbf3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf3b-113">-DefaultProfile</span></span>
<span data-ttu-id="dbf3b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbf3b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf3b-115">CommonParameters</span></span>
<span data-ttu-id="dbf3b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf3b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf3b-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf3b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf3b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbf3b-118">INPUTS</span></span>

## <span data-ttu-id="dbf3b-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbf3b-119">OUTPUTS</span></span>

### <span data-ttu-id="dbf3b-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dbf3b-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dbf3b-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbf3b-121">NOTES</span></span>

## <span data-ttu-id="dbf3b-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbf3b-122">RELATED LINKS</span></span>

[<span data-ttu-id="dbf3b-123">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="dbf3b-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="dbf3b-124">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="dbf3b-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


