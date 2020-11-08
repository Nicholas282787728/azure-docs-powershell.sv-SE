---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: e2a66eef93d2ed59f78e492cac7fa7fac4dd0244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915954"
---
# <span data-ttu-id="4fc18-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4fc18-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="4fc18-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fc18-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc18-103">Ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="4fc18-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="4fc18-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fc18-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fc18-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fc18-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc18-106">Cmdleten **set-AzIntegrationAccountMap** ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="4fc18-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="4fc18-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="4fc18-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="4fc18-108">Ange integrerings konto namnet, resurs gruppens namn och kartans namn.</span><span class="sxs-lookup"><span data-stu-id="4fc18-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="4fc18-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="4fc18-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4fc18-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="4fc18-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4fc18-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="4fc18-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4fc18-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="4fc18-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4fc18-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fc18-113">EXAMPLES</span></span>

### <span data-ttu-id="4fc18-114">Exempel 1: ändra översikt över en integrerings konto</span><span class="sxs-lookup"><span data-stu-id="4fc18-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="4fc18-115">Det här kommandot ändrar mappnings konto översikten i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4fc18-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="4fc18-116">Kommandot anger en kart definition som lagras i $MapContent-variabeln med ett föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="4fc18-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="4fc18-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fc18-117">PARAMETERS</span></span>

### <span data-ttu-id="4fc18-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="4fc18-118">-ContentType</span></span>
<span data-ttu-id="4fc18-119">Anger en innehålls typ för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="4fc18-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="4fc18-120">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="4fc18-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc18-121">-DefaultProfile</span></span>
<span data-ttu-id="4fc18-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4fc18-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fc18-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4fc18-123">-Force</span></span>
<span data-ttu-id="4fc18-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4fc18-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="4fc18-125">-MapDefinition</span></span>
<span data-ttu-id="4fc18-126">Anger ett definitions objekt för integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="4fc18-126">Specifies a definition object for integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="4fc18-127">-MapFilePath</span></span>
<span data-ttu-id="4fc18-128">Anger sökvägen till en definition för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="4fc18-128">Specifies the file path of a definition for the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="4fc18-129">-MapName</span></span>
<span data-ttu-id="4fc18-130">Anger namnet på en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="4fc18-130">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="4fc18-131">-MapType</span></span>
<span data-ttu-id="4fc18-132">Anger typen för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="4fc18-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="4fc18-133">Denna cmdlet stöder XSLT som en typ av karta.</span><span class="sxs-lookup"><span data-stu-id="4fc18-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4fc18-134">-Metadata</span></span>
<span data-ttu-id="4fc18-135">Anger ett metadataobjekt för kartan.</span><span class="sxs-lookup"><span data-stu-id="4fc18-135">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fc18-136">-Name</span></span>
<span data-ttu-id="4fc18-137">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="4fc18-137">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc18-138">-ResourceGroupName</span></span>
<span data-ttu-id="4fc18-139">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4fc18-139">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc18-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fc18-140">-Confirm</span></span>
<span data-ttu-id="4fc18-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fc18-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc18-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc18-142">-WhatIf</span></span>
<span data-ttu-id="4fc18-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4fc18-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc18-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4fc18-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc18-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc18-145">CommonParameters</span></span>
<span data-ttu-id="4fc18-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc18-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc18-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc18-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc18-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fc18-148">INPUTS</span></span>

### <span data-ttu-id="4fc18-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc18-149">System.String</span></span>

## <span data-ttu-id="4fc18-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fc18-150">OUTPUTS</span></span>

### <span data-ttu-id="4fc18-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4fc18-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="4fc18-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fc18-152">NOTES</span></span>

## <span data-ttu-id="4fc18-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fc18-153">RELATED LINKS</span></span>

[<span data-ttu-id="4fc18-154">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4fc18-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="4fc18-155">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4fc18-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="4fc18-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4fc18-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

