---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: 0f87254f72d0b5ac22a5770ad3f1a9d03b70fd34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575308"
---
# <span data-ttu-id="2335d-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2335d-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="2335d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2335d-102">SYNOPSIS</span></span>
<span data-ttu-id="2335d-103">Hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="2335d-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2335d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2335d-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2335d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2335d-105">DESCRIPTION</span></span>
<span data-ttu-id="2335d-106">Cmdleten **Get-AzureRmContainerService** hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="2335d-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="2335d-107">Du kan visa egenskaperna för en behållar tjänst, vilket inkluderar tillstånd, antalet huvud och agenter samt det fullt kvalificerade domän namnet för huvud gruppen och agenten.</span><span class="sxs-lookup"><span data-stu-id="2335d-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="2335d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2335d-108">EXAMPLES</span></span>

### <span data-ttu-id="2335d-109">Exempel 1: skaffa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="2335d-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="2335d-110">Det här kommandot får en behållar tjänst som heter CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="2335d-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="2335d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2335d-111">PARAMETERS</span></span>

### <span data-ttu-id="2335d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2335d-112">-DefaultProfile</span></span>
<span data-ttu-id="2335d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2335d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2335d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2335d-114">-Name</span></span>
<span data-ttu-id="2335d-115">Anger namnet på den behållar tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="2335d-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2335d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2335d-116">-ResourceGroupName</span></span>
<span data-ttu-id="2335d-117">Anger resurs gruppen för den behållar tjänst som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="2335d-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2335d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2335d-118">CommonParameters</span></span>
<span data-ttu-id="2335d-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2335d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2335d-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2335d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2335d-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2335d-121">INPUTS</span></span>

### <span data-ttu-id="2335d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2335d-122">System.String</span></span>

## <span data-ttu-id="2335d-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2335d-123">OUTPUTS</span></span>

### <span data-ttu-id="2335d-124">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2335d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2335d-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2335d-125">NOTES</span></span>

## <span data-ttu-id="2335d-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2335d-126">RELATED LINKS</span></span>

[<span data-ttu-id="2335d-127">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2335d-127">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="2335d-128">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2335d-128">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="2335d-129">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2335d-129">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


