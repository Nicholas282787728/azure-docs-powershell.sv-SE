---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585031"
---
# <span data-ttu-id="82092-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="82092-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="82092-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82092-102">SYNOPSIS</span></span>
<span data-ttu-id="82092-103">Återskapar en inloggnings information för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="82092-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82092-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82092-104">SYNTAX</span></span>

### <span data-ttu-id="82092-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="82092-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82092-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82092-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82092-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82092-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82092-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82092-108">DESCRIPTION</span></span>
<span data-ttu-id="82092-109">Update-AzureRmContainerRegistryCredential cmdlet återskapar inloggnings uppgifter för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="82092-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="82092-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82092-110">EXAMPLES</span></span>

### <span data-ttu-id="82092-111">Exempel 1: återskapa autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="82092-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="82092-112">Det här kommandot återskapar inloggnings uppgifter för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="82092-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="82092-113">Administratörs användaren måste vara aktive rad för att testregistry-registret \` \` ska återskapa inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="82092-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="82092-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82092-114">PARAMETERS</span></span>

### <span data-ttu-id="82092-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82092-115">-DefaultProfile</span></span>
<span data-ttu-id="82092-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="82092-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82092-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="82092-117">-Name</span></span>
<span data-ttu-id="82092-118">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="82092-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="82092-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="82092-119">-PasswordName</span></span>
<span data-ttu-id="82092-120">Namnet på lösen ordet som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="82092-120">The name of password to regenerate.</span></span>
<span data-ttu-id="82092-121">Tillåtna värden: lösen ord, password2.</span><span class="sxs-lookup"><span data-stu-id="82092-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82092-122">-Register</span><span class="sxs-lookup"><span data-stu-id="82092-122">-Registry</span></span>
<span data-ttu-id="82092-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="82092-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="82092-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82092-124">-ResourceGroupName</span></span>
<span data-ttu-id="82092-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="82092-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="82092-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82092-126">-ResourceId</span></span>
<span data-ttu-id="82092-127">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="82092-127">The container registry resource id</span></span>

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

### <span data-ttu-id="82092-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82092-128">-Confirm</span></span>
<span data-ttu-id="82092-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82092-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82092-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82092-130">-WhatIf</span></span>
<span data-ttu-id="82092-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82092-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82092-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82092-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82092-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82092-133">CommonParameters</span></span>
<span data-ttu-id="82092-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82092-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82092-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82092-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82092-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82092-136">INPUTS</span></span>

### <span data-ttu-id="82092-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82092-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="82092-138">Parametrar: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82092-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="82092-139">System. String</span><span class="sxs-lookup"><span data-stu-id="82092-139">System.String</span></span>

## <span data-ttu-id="82092-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82092-140">OUTPUTS</span></span>

### <span data-ttu-id="82092-141">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="82092-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="82092-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82092-142">NOTES</span></span>

## <span data-ttu-id="82092-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82092-143">RELATED LINKS</span></span>

[<span data-ttu-id="82092-144">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82092-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="82092-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82092-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="82092-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="82092-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

