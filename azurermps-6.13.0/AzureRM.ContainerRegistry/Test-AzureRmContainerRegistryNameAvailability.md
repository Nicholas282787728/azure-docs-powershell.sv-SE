---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: 996dfdb0c534369aed47787601f8a2883e2af788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575254"
---
# <span data-ttu-id="13c2f-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="13c2f-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="13c2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="13c2f-103">Kontrollerar tillgänglighet för ett namn på en behållare.</span><span class="sxs-lookup"><span data-stu-id="13c2f-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13c2f-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13c2f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="13c2f-106">Test-AzureRmContainerRegistryNameAvailability cmdlet kontrollerar om ett namn på en behållare är giltig och tillgänglig för användning.</span><span class="sxs-lookup"><span data-stu-id="13c2f-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="13c2f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="13c2f-108">Exempel 1: kontrollerar tillgänglighet för ett namn på en behållares register</span><span class="sxs-lookup"><span data-stu-id="13c2f-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="13c2f-109">Det här kommandot kontrollerar tillgängligheten för behållar register namnet \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="13c2f-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="13c2f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="13c2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c2f-111">-DefaultProfile</span></span>
<span data-ttu-id="13c2f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="13c2f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13c2f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="13c2f-113">-Name</span></span>
<span data-ttu-id="13c2f-114">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="13c2f-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="13c2f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c2f-115">CommonParameters</span></span>
<span data-ttu-id="13c2f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c2f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c2f-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c2f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c2f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13c2f-118">INPUTS</span></span>

### <span data-ttu-id="13c2f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="13c2f-119">System.String</span></span>

## <span data-ttu-id="13c2f-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13c2f-120">OUTPUTS</span></span>

### <span data-ttu-id="13c2f-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="13c2f-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="13c2f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13c2f-122">NOTES</span></span>

## <span data-ttu-id="13c2f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13c2f-123">RELATED LINKS</span></span>

[<span data-ttu-id="13c2f-124">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="13c2f-124">New-AzureRmContainerRegistry</span></span>]()

