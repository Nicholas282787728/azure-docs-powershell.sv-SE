---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273359"
---
# <span data-ttu-id="18907-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18907-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="18907-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18907-102">SYNOPSIS</span></span>
<span data-ttu-id="18907-103">Ändrar ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="18907-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="18907-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18907-104">SYNTAX</span></span>

### <span data-ttu-id="18907-105">ByIntegrationAccountAndFilePath (standard)</span><span class="sxs-lookup"><span data-stu-id="18907-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18907-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="18907-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18907-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="18907-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18907-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="18907-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18907-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="18907-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18907-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="18907-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18907-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="18907-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18907-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="18907-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18907-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="18907-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18907-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18907-114">DESCRIPTION</span></span>
<span data-ttu-id="18907-115">Cmdleten **set-AzIntegrationAccountAssembly** ändrar ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="18907-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="18907-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18907-116">EXAMPLES</span></span>

### <span data-ttu-id="18907-117">Exempel 1: ändra en sammansättning med lokal fil</span><span class="sxs-lookup"><span data-stu-id="18907-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="18907-118">Ändrar sammansättningen "sampleAssembly" med den lokala filen som finns på fil Sök vägen i "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="18907-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="18907-119">Exempel 2: ändra en sammansättning med byte data</span><span class="sxs-lookup"><span data-stu-id="18907-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="18907-120">Ändrar sammansättningen "sampleAssembly" med en byte mat ris som finns i "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="18907-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="18907-121">Exempel 3: ändra en sammansättning med hjälp av en innehålls länk</span><span class="sxs-lookup"><span data-stu-id="18907-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="18907-122">Ändrar sammansättningen "sampleAssembly" med hjälp av en byte-data som finns på URL-adressen "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="18907-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="18907-123">Det här är den rekommenderade metoden för att skapa paket med stor storlek.</span><span class="sxs-lookup"><span data-stu-id="18907-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="18907-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18907-124">PARAMETERS</span></span>

### <span data-ttu-id="18907-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="18907-125">-AssemblyData</span></span>
<span data-ttu-id="18907-126">Information om byte av integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="18907-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="18907-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="18907-127">-AssemblyFilePath</span></span>
<span data-ttu-id="18907-128">Sökvägen till integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="18907-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="18907-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="18907-129">-ContentLink</span></span>
<span data-ttu-id="18907-130">En allmänt tillgänglig länk till integrerings kontots monterings data.</span><span class="sxs-lookup"><span data-stu-id="18907-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="18907-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18907-131">-DefaultProfile</span></span>
<span data-ttu-id="18907-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18907-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18907-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18907-133">-InputObject</span></span>
<span data-ttu-id="18907-134">Ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="18907-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18907-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="18907-135">-Metadata</span></span>
<span data-ttu-id="18907-136">Alla metadata för integrerings konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="18907-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="18907-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="18907-137">-Name</span></span>
<span data-ttu-id="18907-138">Namnet på integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="18907-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18907-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="18907-139">-ParentName</span></span>
<span data-ttu-id="18907-140">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="18907-140">The integration account name.</span></span>

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

### <span data-ttu-id="18907-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18907-141">-ResourceGroupName</span></span>
<span data-ttu-id="18907-142">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="18907-142">The resource group name.</span></span>

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

### <span data-ttu-id="18907-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18907-143">-ResourceId</span></span>
<span data-ttu-id="18907-144">ID för sammansättningen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="18907-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="18907-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18907-145">-Confirm</span></span>
<span data-ttu-id="18907-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18907-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18907-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18907-147">-WhatIf</span></span>
<span data-ttu-id="18907-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18907-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18907-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18907-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18907-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18907-150">CommonParameters</span></span>
<span data-ttu-id="18907-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18907-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18907-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18907-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18907-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18907-153">INPUTS</span></span>

### <span data-ttu-id="18907-154">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18907-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="18907-155">System. String</span><span class="sxs-lookup"><span data-stu-id="18907-155">System.String</span></span>

## <span data-ttu-id="18907-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18907-156">OUTPUTS</span></span>

### <span data-ttu-id="18907-157">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="18907-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="18907-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18907-158">NOTES</span></span>

## <span data-ttu-id="18907-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18907-159">RELATED LINKS</span></span>
