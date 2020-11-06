---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572863"
---
# <span data-ttu-id="9ac27-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9ac27-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="9ac27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ac27-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac27-103">Hämtar inloggnings uppgifterna för en behållar-register.</span><span class="sxs-lookup"><span data-stu-id="9ac27-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ac27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ac27-104">SYNTAX</span></span>

### <span data-ttu-id="9ac27-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9ac27-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac27-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ac27-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac27-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ac27-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac27-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ac27-108">DESCRIPTION</span></span>
<span data-ttu-id="9ac27-109">Med cmdleten Get-AzureRmContainerRegistryCredential får du inloggnings uppgifterna för en behållar register.</span><span class="sxs-lookup"><span data-stu-id="9ac27-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="9ac27-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ac27-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac27-111">Exempel 1: Hämta autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="9ac27-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="9ac27-112">Det här kommandot får inloggnings uppgifterna för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="9ac27-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="9ac27-113">Administratörs användaren måste vara aktive rad för registret för behållarna Registry \` \` för att få inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="9ac27-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="9ac27-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ac27-114">PARAMETERS</span></span>

### <span data-ttu-id="9ac27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac27-115">-DefaultProfile</span></span>
<span data-ttu-id="9ac27-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9ac27-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ac27-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ac27-117">-Name</span></span>
<span data-ttu-id="9ac27-118">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="9ac27-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="9ac27-119">-Register</span><span class="sxs-lookup"><span data-stu-id="9ac27-119">-Registry</span></span>
<span data-ttu-id="9ac27-120">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="9ac27-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="9ac27-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac27-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ac27-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9ac27-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ac27-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ac27-123">-ResourceId</span></span>
<span data-ttu-id="9ac27-124">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="9ac27-124">The container registry resource id</span></span>

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

### <span data-ttu-id="9ac27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac27-125">CommonParameters</span></span>
<span data-ttu-id="9ac27-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac27-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac27-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac27-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ac27-128">INPUTS</span></span>

### <span data-ttu-id="9ac27-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9ac27-129">System.String</span></span>

## <span data-ttu-id="9ac27-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ac27-130">OUTPUTS</span></span>

### <span data-ttu-id="9ac27-131">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9ac27-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="9ac27-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ac27-132">NOTES</span></span>

## <span data-ttu-id="9ac27-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ac27-133">RELATED LINKS</span></span>

[<span data-ttu-id="9ac27-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9ac27-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="9ac27-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9ac27-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="9ac27-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9ac27-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

