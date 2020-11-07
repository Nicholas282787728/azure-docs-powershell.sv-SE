---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: 1ef273329634e080c4117b9ddd0d1eaf8d91bb0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758253"
---
# <span data-ttu-id="65531-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="65531-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="65531-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65531-102">SYNOPSIS</span></span>
<span data-ttu-id="65531-103">Hämtar lagrings resursanvändningen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="65531-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65531-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65531-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65531-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65531-105">DESCRIPTION</span></span>
<span data-ttu-id="65531-106">Cmdleten **Get-AzureRmStorageUsage** hämtar resursanvändningen för Azure Storage för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="65531-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="65531-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65531-107">EXAMPLES</span></span>

### <span data-ttu-id="65531-108">Exempel 1: skaffa användning av lagrings resurser</span><span class="sxs-lookup"><span data-stu-id="65531-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="65531-109">Det här kommandot får användning av lagrings resurserna för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="65531-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="65531-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65531-110">PARAMETERS</span></span>

### <span data-ttu-id="65531-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65531-111">-DefaultProfile</span></span>
<span data-ttu-id="65531-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65531-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65531-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65531-113">CommonParameters</span></span>
<span data-ttu-id="65531-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65531-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65531-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65531-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65531-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65531-116">INPUTS</span></span>

## <span data-ttu-id="65531-117">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65531-117">OUTPUTS</span></span>

## <span data-ttu-id="65531-118">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65531-118">NOTES</span></span>

## <span data-ttu-id="65531-119">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65531-119">RELATED LINKS</span></span>

[<span data-ttu-id="65531-120">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="65531-120">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


