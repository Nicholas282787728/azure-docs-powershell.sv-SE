---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263310"
---
# <span data-ttu-id="186ea-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="186ea-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="186ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="186ea-102">SYNOPSIS</span></span>
<span data-ttu-id="186ea-103">Hämtar inloggnings uppgifterna för en behållar-register.</span><span class="sxs-lookup"><span data-stu-id="186ea-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="186ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="186ea-104">SYNTAX</span></span>

### <span data-ttu-id="186ea-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="186ea-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="186ea-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="186ea-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="186ea-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="186ea-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="186ea-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="186ea-108">DESCRIPTION</span></span>
<span data-ttu-id="186ea-109">Med cmdleten Get-AzContainerRegistryCredential får du inloggnings uppgifterna för en behållar register.</span><span class="sxs-lookup"><span data-stu-id="186ea-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="186ea-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="186ea-110">EXAMPLES</span></span>

### <span data-ttu-id="186ea-111">Exempel 1: Hämta autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="186ea-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="186ea-112">Det här kommandot får inloggnings uppgifterna för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="186ea-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="186ea-113">Administratörs användaren måste vara aktive rad för registret för behållarna Registry \` \` för att få inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="186ea-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="186ea-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="186ea-114">PARAMETERS</span></span>

### <span data-ttu-id="186ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186ea-115">-DefaultProfile</span></span>
<span data-ttu-id="186ea-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="186ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="186ea-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="186ea-117">-Name</span></span>
<span data-ttu-id="186ea-118">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="186ea-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="186ea-119">-Register</span><span class="sxs-lookup"><span data-stu-id="186ea-119">-Registry</span></span>
<span data-ttu-id="186ea-120">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="186ea-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="186ea-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="186ea-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="186ea-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="186ea-123">-ResourceId</span></span>
<span data-ttu-id="186ea-124">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="186ea-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186ea-125">CommonParameters</span></span>
<span data-ttu-id="186ea-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186ea-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="186ea-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186ea-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="186ea-128">INPUTS</span></span>

### <span data-ttu-id="186ea-129">System. String</span><span class="sxs-lookup"><span data-stu-id="186ea-129">System.String</span></span>

## <span data-ttu-id="186ea-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="186ea-130">OUTPUTS</span></span>

### <span data-ttu-id="186ea-131">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="186ea-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="186ea-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="186ea-132">NOTES</span></span>

## <span data-ttu-id="186ea-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="186ea-133">RELATED LINKS</span></span>

[<span data-ttu-id="186ea-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="186ea-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="186ea-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="186ea-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="186ea-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="186ea-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

