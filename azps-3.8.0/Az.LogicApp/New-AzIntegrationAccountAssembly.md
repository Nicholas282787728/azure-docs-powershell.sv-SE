---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092064"
---
# <span data-ttu-id="6c178-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6c178-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="6c178-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c178-102">SYNOPSIS</span></span>
<span data-ttu-id="6c178-103">Skapar ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="6c178-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="6c178-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c178-104">SYNTAX</span></span>

### <span data-ttu-id="6c178-105">ByIntegrationAccountAndFilePath (standard)</span><span class="sxs-lookup"><span data-stu-id="6c178-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c178-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="6c178-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c178-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="6c178-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c178-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="6c178-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c178-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="6c178-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c178-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6c178-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c178-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="6c178-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c178-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="6c178-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c178-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6c178-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c178-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c178-114">DESCRIPTION</span></span>
<span data-ttu-id="6c178-115">Cmdleten **Get-AzIntegrationAccountAssembly** skapar en ny sammansättning i ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="6c178-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="6c178-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c178-116">EXAMPLES</span></span>

### <span data-ttu-id="6c178-117">Exempel 1: skapa ny sammansättning med lokal fil</span><span class="sxs-lookup"><span data-stu-id="6c178-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="6c178-118">Skapar en ny sammansättning med den lokala filen som finns på fil Sök vägen i $localAssemblyFilePath.</span><span class="sxs-lookup"><span data-stu-id="6c178-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="6c178-119">Exempel 2: skapa ny sammansättning med byte data</span><span class="sxs-lookup"><span data-stu-id="6c178-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="6c178-120">Skapar en ny sammansättning med en byte mat ris med "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="6c178-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="6c178-121">Exempel 3: skapa ny sammansättning med hjälp av en innehålls länk</span><span class="sxs-lookup"><span data-stu-id="6c178-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="6c178-122">Skapar en ny sammansättning med en byte-data som finns på URL-adressen "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="6c178-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="6c178-123">Det här är den rekommenderade metoden för att skapa paket med stor storlek.</span><span class="sxs-lookup"><span data-stu-id="6c178-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="6c178-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c178-124">PARAMETERS</span></span>

### <span data-ttu-id="6c178-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="6c178-125">-AssemblyData</span></span>
<span data-ttu-id="6c178-126">Information om byte av integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="6c178-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="6c178-127">-AssemblyFilePath</span></span>
<span data-ttu-id="6c178-128">Sökvägen till integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="6c178-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="6c178-129">-ContentLink</span></span>
<span data-ttu-id="6c178-130">En allmänt tillgänglig länk till integrerings kontots monterings data.</span><span class="sxs-lookup"><span data-stu-id="6c178-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c178-131">-DefaultProfile</span></span>
<span data-ttu-id="6c178-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c178-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c178-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6c178-133">-Metadata</span></span>
<span data-ttu-id="6c178-134">Alla metadata för integrerings konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="6c178-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="6c178-135">-Name</span></span>
<span data-ttu-id="6c178-136">Namnet på integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="6c178-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="6c178-137">-ParentName</span></span>
<span data-ttu-id="6c178-138">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="6c178-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6c178-139">-ParentObject</span></span>
<span data-ttu-id="6c178-140">Ett integrations konto objekt.</span><span class="sxs-lookup"><span data-stu-id="6c178-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6c178-141">-ParentResourceId</span></span>
<span data-ttu-id="6c178-142">ID för integrations konto.</span><span class="sxs-lookup"><span data-stu-id="6c178-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c178-143">-ResourceGroupName</span></span>
<span data-ttu-id="6c178-144">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6c178-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c178-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c178-145">-Confirm</span></span>
<span data-ttu-id="6c178-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c178-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c178-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c178-147">-WhatIf</span></span>
<span data-ttu-id="6c178-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c178-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c178-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c178-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c178-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c178-150">CommonParameters</span></span>
<span data-ttu-id="6c178-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c178-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c178-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c178-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c178-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c178-153">INPUTS</span></span>

### <span data-ttu-id="6c178-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6c178-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="6c178-155">System. String</span><span class="sxs-lookup"><span data-stu-id="6c178-155">System.String</span></span>

## <span data-ttu-id="6c178-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c178-156">OUTPUTS</span></span>

### <span data-ttu-id="6c178-157">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6c178-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="6c178-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c178-158">NOTES</span></span>

## <span data-ttu-id="6c178-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c178-159">RELATED LINKS</span></span>