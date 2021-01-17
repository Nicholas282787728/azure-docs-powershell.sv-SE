---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416699"
---
# <span data-ttu-id="551a5-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="551a5-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="551a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="551a5-102">SYNOPSIS</span></span>
<span data-ttu-id="551a5-103">Återskapar en inloggnings information för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="551a5-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="551a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="551a5-104">SYNTAX</span></span>

### <span data-ttu-id="551a5-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="551a5-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="551a5-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="551a5-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551a5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="551a5-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551a5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="551a5-108">DESCRIPTION</span></span>
<span data-ttu-id="551a5-109">Update-AzContainerRegistryCredential cmdlet återskapar inloggnings uppgifter för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="551a5-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="551a5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="551a5-110">EXAMPLES</span></span>

### <span data-ttu-id="551a5-111">Exempel 1: återskapa autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="551a5-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="551a5-112">Det här kommandot återskapar inloggnings uppgifter för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="551a5-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="551a5-113">Administratörs användaren måste vara aktive rad för att testregistry-registret \` \` ska återskapa inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="551a5-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="551a5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="551a5-114">PARAMETERS</span></span>

### <span data-ttu-id="551a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551a5-115">-DefaultProfile</span></span>
<span data-ttu-id="551a5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="551a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="551a5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="551a5-117">-Name</span></span>
<span data-ttu-id="551a5-118">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="551a5-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="551a5-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="551a5-119">-PasswordName</span></span>
<span data-ttu-id="551a5-120">Namnet på lösen ordet som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="551a5-120">The name of password to regenerate.</span></span>
<span data-ttu-id="551a5-121">Tillåtna värden: lösen ord, password2.</span><span class="sxs-lookup"><span data-stu-id="551a5-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="551a5-122">-Register</span><span class="sxs-lookup"><span data-stu-id="551a5-122">-Registry</span></span>
<span data-ttu-id="551a5-123">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="551a5-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="551a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="551a5-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="551a5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="551a5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="551a5-126">-ResourceId</span></span>
<span data-ttu-id="551a5-127">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="551a5-127">The container registry resource id</span></span>

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

### <span data-ttu-id="551a5-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="551a5-128">-Confirm</span></span>
<span data-ttu-id="551a5-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="551a5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="551a5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551a5-130">-WhatIf</span></span>
<span data-ttu-id="551a5-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="551a5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="551a5-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="551a5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="551a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551a5-133">CommonParameters</span></span>
<span data-ttu-id="551a5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551a5-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="551a5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551a5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="551a5-136">INPUTS</span></span>

### <span data-ttu-id="551a5-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="551a5-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="551a5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="551a5-138">System.String</span></span>

## <span data-ttu-id="551a5-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="551a5-139">OUTPUTS</span></span>

### <span data-ttu-id="551a5-140">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="551a5-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="551a5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="551a5-141">NOTES</span></span>

## <span data-ttu-id="551a5-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="551a5-142">RELATED LINKS</span></span>

[<span data-ttu-id="551a5-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="551a5-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="551a5-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="551a5-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="551a5-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="551a5-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

