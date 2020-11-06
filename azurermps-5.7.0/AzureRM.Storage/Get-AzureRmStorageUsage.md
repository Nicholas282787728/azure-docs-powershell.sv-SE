---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: 5d44fa0a3e0ead373a822ae91080df9bdc60cc50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581915"
---
# <span data-ttu-id="45465-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="45465-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="45465-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45465-102">SYNOPSIS</span></span>
<span data-ttu-id="45465-103">Hämtar lagrings resursanvändningen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="45465-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45465-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45465-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45465-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45465-105">DESCRIPTION</span></span>
<span data-ttu-id="45465-106">Cmdleten **Get-AzureRmStorageUsage** hämtar resursanvändningen för Azure Storage för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="45465-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="45465-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45465-107">EXAMPLES</span></span>

### <span data-ttu-id="45465-108">Exempel 1: skaffa användning av lagrings resurser</span><span class="sxs-lookup"><span data-stu-id="45465-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="45465-109">Det här kommandot får användning av lagrings resurserna för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="45465-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="45465-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45465-110">PARAMETERS</span></span>

### <span data-ttu-id="45465-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45465-111">-DefaultProfile</span></span>
<span data-ttu-id="45465-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45465-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45465-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45465-113">CommonParameters</span></span>
<span data-ttu-id="45465-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45465-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45465-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45465-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45465-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45465-116">INPUTS</span></span>

### <span data-ttu-id="45465-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="45465-117">None</span></span>
<span data-ttu-id="45465-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="45465-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45465-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45465-119">OUTPUTS</span></span>

### <span data-ttu-id="45465-120">Microsoft. Azure. commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="45465-120">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="45465-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45465-121">NOTES</span></span>

## <span data-ttu-id="45465-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45465-122">RELATED LINKS</span></span>

[<span data-ttu-id="45465-123">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="45465-123">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


