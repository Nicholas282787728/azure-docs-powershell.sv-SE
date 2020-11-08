---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259714"
---
# <span data-ttu-id="57916-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="57916-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="57916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57916-102">SYNOPSIS</span></span>
<span data-ttu-id="57916-103">Kontrollerar tillgänglighet för ett namn på en behållare.</span><span class="sxs-lookup"><span data-stu-id="57916-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="57916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57916-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57916-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57916-105">DESCRIPTION</span></span>
<span data-ttu-id="57916-106">Test-AzContainerRegistryNameAvailability cmdlet kontrollerar om ett namn på en behållare är giltig och tillgänglig för användning.</span><span class="sxs-lookup"><span data-stu-id="57916-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="57916-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57916-107">EXAMPLES</span></span>

### <span data-ttu-id="57916-108">Exempel 1: kontrollerar tillgänglighet för ett namn på en behållares register</span><span class="sxs-lookup"><span data-stu-id="57916-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="57916-109">Det här kommandot kontrollerar tillgängligheten för behållar register namnet \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="57916-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="57916-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57916-110">PARAMETERS</span></span>

### <span data-ttu-id="57916-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57916-111">-DefaultProfile</span></span>
<span data-ttu-id="57916-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57916-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57916-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="57916-113">-Name</span></span>
<span data-ttu-id="57916-114">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="57916-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57916-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57916-115">CommonParameters</span></span>
<span data-ttu-id="57916-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57916-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57916-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57916-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57916-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57916-118">INPUTS</span></span>

### <span data-ttu-id="57916-119">System. String</span><span class="sxs-lookup"><span data-stu-id="57916-119">System.String</span></span>

## <span data-ttu-id="57916-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57916-120">OUTPUTS</span></span>

### <span data-ttu-id="57916-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="57916-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="57916-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57916-122">NOTES</span></span>

## <span data-ttu-id="57916-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57916-123">RELATED LINKS</span></span>

[<span data-ttu-id="57916-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="57916-124">New-AzContainerRegistry</span></span>]()

