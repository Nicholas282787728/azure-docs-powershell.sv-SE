---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578243"
---
# <span data-ttu-id="20134-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="20134-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="20134-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20134-102">SYNOPSIS</span></span>
<span data-ttu-id="20134-103">Kontrollerar tillgänglighet för ett namn på en behållare.</span><span class="sxs-lookup"><span data-stu-id="20134-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20134-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20134-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20134-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20134-105">DESCRIPTION</span></span>
<span data-ttu-id="20134-106">Test-AzureRmContainerRegistryNameAvailability cmdlet kontrollerar om ett namn på en behållare är giltig och tillgänglig för användning.</span><span class="sxs-lookup"><span data-stu-id="20134-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="20134-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20134-107">EXAMPLES</span></span>

### <span data-ttu-id="20134-108">Exempel 1: kontrollerar tillgänglighet för ett namn på en behållares register</span><span class="sxs-lookup"><span data-stu-id="20134-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="20134-109">Det här kommandot kontrollerar tillgängligheten för behållar register namnet \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="20134-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="20134-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20134-110">PARAMETERS</span></span>

### <span data-ttu-id="20134-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="20134-111">-Name</span></span>
<span data-ttu-id="20134-112">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="20134-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20134-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20134-113">-DefaultProfile</span></span>
<span data-ttu-id="20134-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20134-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20134-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20134-115">CommonParameters</span></span>
<span data-ttu-id="20134-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20134-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20134-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20134-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20134-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20134-118">INPUTS</span></span>

### <span data-ttu-id="20134-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="20134-119">None</span></span>
<span data-ttu-id="20134-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="20134-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20134-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20134-121">OUTPUTS</span></span>

### <span data-ttu-id="20134-122">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="20134-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="20134-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20134-123">NOTES</span></span>

## <span data-ttu-id="20134-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20134-124">RELATED LINKS</span></span>

[<span data-ttu-id="20134-125">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="20134-125">New-AzureRmContainerRegistry</span></span>]()

