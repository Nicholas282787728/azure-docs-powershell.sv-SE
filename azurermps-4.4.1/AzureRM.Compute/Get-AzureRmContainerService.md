---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 3bdb0a0f497f6e7a6ebff4b4d449e75fa759f7a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757807"
---
# <span data-ttu-id="9047e-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9047e-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="9047e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9047e-102">SYNOPSIS</span></span>
<span data-ttu-id="9047e-103">Hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="9047e-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9047e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9047e-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9047e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9047e-105">DESCRIPTION</span></span>
<span data-ttu-id="9047e-106">Cmdleten **Get-AzureRmContainerService** hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="9047e-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="9047e-107">Du kan visa egenskaperna för en behållar tjänst, vilket inkluderar tillstånd, antalet huvud och agenter samt det fullt kvalificerade domän namnet för huvud gruppen och agenten.</span><span class="sxs-lookup"><span data-stu-id="9047e-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="9047e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9047e-108">EXAMPLES</span></span>

### <span data-ttu-id="9047e-109">Exempel 1: skaffa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="9047e-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="9047e-110">Det här kommandot får en behållar tjänst som heter CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="9047e-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="9047e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9047e-111">PARAMETERS</span></span>

### <span data-ttu-id="9047e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9047e-112">-DefaultProfile</span></span>
<span data-ttu-id="9047e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9047e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9047e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9047e-114">-Name</span></span>
<span data-ttu-id="9047e-115">Anger namnet på den behållar tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9047e-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9047e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9047e-116">-ResourceGroupName</span></span>
<span data-ttu-id="9047e-117">Anger resurs gruppen för den behållar tjänst som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="9047e-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9047e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9047e-118">CommonParameters</span></span>
<span data-ttu-id="9047e-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9047e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9047e-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9047e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9047e-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9047e-121">INPUTS</span></span>

## <span data-ttu-id="9047e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9047e-122">OUTPUTS</span></span>

## <span data-ttu-id="9047e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9047e-123">NOTES</span></span>

## <span data-ttu-id="9047e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9047e-124">RELATED LINKS</span></span>

[<span data-ttu-id="9047e-125">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9047e-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="9047e-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9047e-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="9047e-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9047e-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


