---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579744"
---
# <span data-ttu-id="44b87-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="44b87-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="44b87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44b87-102">SYNOPSIS</span></span>
<span data-ttu-id="44b87-103">Hämtar inloggnings uppgifterna för en behållar-register.</span><span class="sxs-lookup"><span data-stu-id="44b87-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44b87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44b87-104">SYNTAX</span></span>

### <span data-ttu-id="44b87-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="44b87-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b87-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b87-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44b87-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44b87-107">DESCRIPTION</span></span>
<span data-ttu-id="44b87-108">Cmdleten **Get-AzureRmContainerRegistryCredential** hämtar autentiseringsuppgifterna för inloggning för en behållar-register.</span><span class="sxs-lookup"><span data-stu-id="44b87-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="44b87-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44b87-109">EXAMPLES</span></span>

### <span data-ttu-id="44b87-110">Exempel 1: Hämta autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="44b87-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="44b87-111">Det här kommandot får inloggnings uppgifterna för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="44b87-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="44b87-112">Administratörs användaren måste vara aktive rad för att behållar registret `MyRegistry` ska kunna ange inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="44b87-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="44b87-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44b87-113">PARAMETERS</span></span>

### <span data-ttu-id="44b87-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="44b87-114">-Name</span></span>
<span data-ttu-id="44b87-115">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="44b87-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b87-116">-Register</span><span class="sxs-lookup"><span data-stu-id="44b87-116">-Registry</span></span>
<span data-ttu-id="44b87-117">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="44b87-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44b87-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b87-118">-ResourceGroupName</span></span>
<span data-ttu-id="44b87-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="44b87-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b87-120">-DefaultProfile</span></span>
<span data-ttu-id="44b87-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44b87-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44b87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b87-122">CommonParameters</span></span>
<span data-ttu-id="44b87-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b87-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44b87-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b87-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44b87-125">INPUTS</span></span>

### <span data-ttu-id="44b87-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44b87-126">PSContainerRegistry</span></span>
<span data-ttu-id="44b87-127">Parametern ' Registry ' godkänner värdet av typen ' PSContainerRegistry ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="44b87-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="44b87-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44b87-128">OUTPUTS</span></span>

### <span data-ttu-id="44b87-129">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="44b87-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="44b87-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44b87-130">NOTES</span></span>

## <span data-ttu-id="44b87-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44b87-131">RELATED LINKS</span></span>

[<span data-ttu-id="44b87-132">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44b87-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="44b87-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44b87-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="44b87-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="44b87-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

