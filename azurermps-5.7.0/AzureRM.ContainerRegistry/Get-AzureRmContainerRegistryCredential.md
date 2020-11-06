---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 68ef1cf00adeec785faf3c3f43ff2e7dbcaafbc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584387"
---
# <span data-ttu-id="095f1-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="095f1-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="095f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="095f1-102">SYNOPSIS</span></span>
<span data-ttu-id="095f1-103">Hämtar inloggnings uppgifterna för en behållar-register.</span><span class="sxs-lookup"><span data-stu-id="095f1-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="095f1-104">SYNTAX</span></span>

### <span data-ttu-id="095f1-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="095f1-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095f1-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="095f1-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="095f1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="095f1-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="095f1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="095f1-108">DESCRIPTION</span></span>
<span data-ttu-id="095f1-109">Med cmdleten Get-AzureRmContainerRegistryCredential får du inloggnings uppgifterna för en behållar register.</span><span class="sxs-lookup"><span data-stu-id="095f1-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="095f1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="095f1-110">EXAMPLES</span></span>

### <span data-ttu-id="095f1-111">Exempel 1: Hämta autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="095f1-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="095f1-112">Det här kommandot får inloggnings uppgifterna för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="095f1-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="095f1-113">Administratörs användaren måste vara aktive rad för registret för behållarna Registry \` \` för att få inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="095f1-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="095f1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="095f1-114">PARAMETERS</span></span>

### <span data-ttu-id="095f1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="095f1-115">-Name</span></span>
<span data-ttu-id="095f1-116">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="095f1-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f1-117">-Register</span><span class="sxs-lookup"><span data-stu-id="095f1-117">-Registry</span></span>
<span data-ttu-id="095f1-118">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="095f1-118">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="095f1-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="095f1-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095f1-121">-DefaultProfile</span></span>
<span data-ttu-id="095f1-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="095f1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="095f1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="095f1-123">-ResourceId</span></span>
<span data-ttu-id="095f1-124">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="095f1-124">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095f1-125">CommonParameters</span></span>
<span data-ttu-id="095f1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095f1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095f1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095f1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="095f1-128">INPUTS</span></span>

### <span data-ttu-id="095f1-129">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="095f1-129">PSContainerRegistry</span></span>
<span data-ttu-id="095f1-130">Parametern ' Registry ' godkänner värdet av typen ' PSContainerRegistry ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="095f1-130">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="095f1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="095f1-131">OUTPUTS</span></span>

### <span data-ttu-id="095f1-132">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="095f1-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="095f1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="095f1-133">NOTES</span></span>

## <span data-ttu-id="095f1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="095f1-134">RELATED LINKS</span></span>

[<span data-ttu-id="095f1-135">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="095f1-135">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="095f1-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="095f1-136">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="095f1-137">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="095f1-137">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

