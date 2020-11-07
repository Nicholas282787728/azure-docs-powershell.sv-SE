---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755937"
---
# <span data-ttu-id="4efd3-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4efd3-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="4efd3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4efd3-102">SYNOPSIS</span></span>
<span data-ttu-id="4efd3-103">Återskapar en inloggnings information för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="4efd3-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4efd3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4efd3-104">SYNTAX</span></span>

### <span data-ttu-id="4efd3-105">NameResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4efd3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4efd3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4efd3-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efd3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4efd3-107">DESCRIPTION</span></span>
<span data-ttu-id="4efd3-108">Cmdleten **Update-AzureRmContainerRegistryCredential** genererar om autentiseringsuppgifter för en behållar registrering.</span><span class="sxs-lookup"><span data-stu-id="4efd3-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="4efd3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4efd3-109">EXAMPLES</span></span>

### <span data-ttu-id="4efd3-110">Exempel 1: återskapa autentiseringsuppgifter för inloggning för en behållar register</span><span class="sxs-lookup"><span data-stu-id="4efd3-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="4efd3-111">Det här kommandot återskapar inloggnings uppgifter för den angivna behållar registret.</span><span class="sxs-lookup"><span data-stu-id="4efd3-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="4efd3-112">Administratörs användaren måste vara aktive rad för att behållar registret `MyRegistry` ska kunna återskapa inloggnings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="4efd3-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="4efd3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4efd3-113">PARAMETERS</span></span>

### <span data-ttu-id="4efd3-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="4efd3-114">-Name</span></span>
<span data-ttu-id="4efd3-115">Namn på behållarens register.</span><span class="sxs-lookup"><span data-stu-id="4efd3-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="4efd3-116">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="4efd3-116">-PasswordName</span></span>
<span data-ttu-id="4efd3-117">Namnet på lösen ordet som ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="4efd3-117">The name of password to regenerate.</span></span>
<span data-ttu-id="4efd3-118">Tillåtna värden: lösen ord, password2.</span><span class="sxs-lookup"><span data-stu-id="4efd3-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efd3-119">-Register</span><span class="sxs-lookup"><span data-stu-id="4efd3-119">-Registry</span></span>
<span data-ttu-id="4efd3-120">Behållarobjekt för container.</span><span class="sxs-lookup"><span data-stu-id="4efd3-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="4efd3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4efd3-121">-ResourceGroupName</span></span>
<span data-ttu-id="4efd3-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4efd3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="4efd3-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4efd3-123">-Confirm</span></span>
<span data-ttu-id="4efd3-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4efd3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efd3-125">-WhatIf</span></span>
<span data-ttu-id="4efd3-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4efd3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4efd3-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4efd3-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efd3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efd3-128">-DefaultProfile</span></span>
<span data-ttu-id="4efd3-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4efd3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4efd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efd3-130">CommonParameters</span></span>
<span data-ttu-id="4efd3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efd3-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4efd3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efd3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4efd3-133">INPUTS</span></span>

### <span data-ttu-id="4efd3-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4efd3-134">PSContainerRegistry</span></span>
<span data-ttu-id="4efd3-135">Parametern ' Registry ' godkänner värdet av typen ' PSContainerRegistry ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4efd3-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="4efd3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4efd3-136">OUTPUTS</span></span>

### <span data-ttu-id="4efd3-137">Microsoft. Azure. commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4efd3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="4efd3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4efd3-138">NOTES</span></span>

## <span data-ttu-id="4efd3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4efd3-139">RELATED LINKS</span></span>

[<span data-ttu-id="4efd3-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4efd3-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="4efd3-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4efd3-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="4efd3-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4efd3-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

