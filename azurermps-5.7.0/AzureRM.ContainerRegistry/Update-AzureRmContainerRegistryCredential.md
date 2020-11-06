---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578260"
---
# <span data-ttu-id="5c4f8-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5c4f8-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="5c4f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4f8-103">Återskapar en inloggnings information för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c4f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c4f8-104">SYNTAX</span></span>

### <span data-ttu-id="5c4f8-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5c4f8-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c4f8-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c4f8-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c4f8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c4f8-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c4f8-108">DESCRIPTION</span></span>
<span data-ttu-id="5c4f8-109">Update-AzureRmContainerRegistryCredential cmdlet återskapar inloggnings uppgifter för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="5c4f8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c4f8-110">EXAMPLES</span></span>

### <span data-ttu-id="5c4f8-111">Exempel 1: återskapa autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="5c4f8-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="5c4f8-112">Det här kommandot återskapar inloggnings uppgifter för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="5c4f8-113">Administratörs användaren måste vara aktive rad för att testregistry-registret \` \` ska återskapa inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="5c4f8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c4f8-114">PARAMETERS</span></span>

### <span data-ttu-id="5c4f8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c4f8-115">-Name</span></span>
<span data-ttu-id="5c4f8-116">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-116">Container Registry Name.</span></span>

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

### <span data-ttu-id="5c4f8-117">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="5c4f8-117">-PasswordName</span></span>
<span data-ttu-id="5c4f8-118">Namnet på lösen ordet som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-118">The name of password to regenerate.</span></span>
<span data-ttu-id="5c4f8-119">Tillåtna värden: lösen ord, password2.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f8-120">-Register</span><span class="sxs-lookup"><span data-stu-id="5c4f8-120">-Registry</span></span>
<span data-ttu-id="5c4f8-121">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c4f8-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c4f8-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c4f8-124">-Confirm</span></span>
<span data-ttu-id="5c4f8-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4f8-126">-WhatIf</span></span>
<span data-ttu-id="5c4f8-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4f8-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4f8-129">-DefaultProfile</span></span>
<span data-ttu-id="5c4f8-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5c4f8-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c4f8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c4f8-131">-ResourceId</span></span>
<span data-ttu-id="5c4f8-132">Resurs-ID för behållar registret</span><span class="sxs-lookup"><span data-stu-id="5c4f8-132">The container registry resource id</span></span>

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

### <span data-ttu-id="5c4f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4f8-133">CommonParameters</span></span>
<span data-ttu-id="5c4f8-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4f8-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c4f8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4f8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c4f8-136">INPUTS</span></span>

### <span data-ttu-id="5c4f8-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c4f8-137">PSContainerRegistry</span></span>
<span data-ttu-id="5c4f8-138">Parametern ' Registry ' godkänner värdet av typen ' PSContainerRegistry ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5c4f8-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="5c4f8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c4f8-139">OUTPUTS</span></span>

### <span data-ttu-id="5c4f8-140">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5c4f8-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="5c4f8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c4f8-141">NOTES</span></span>

## <span data-ttu-id="5c4f8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c4f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="5c4f8-143">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c4f8-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="5c4f8-144">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c4f8-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="5c4f8-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="5c4f8-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

