---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102804"
---
# <span data-ttu-id="d6697-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d6697-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="d6697-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6697-102">SYNOPSIS</span></span>
<span data-ttu-id="d6697-103">Ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="d6697-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="d6697-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6697-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6697-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6697-105">DESCRIPTION</span></span>
<span data-ttu-id="d6697-106">Cmdleten **set-AzIntegrationAccountMap** ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="d6697-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="d6697-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="d6697-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="d6697-108">Ange integrerings konto namnet, resurs gruppens namn och kartans namn.</span><span class="sxs-lookup"><span data-stu-id="d6697-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="d6697-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="d6697-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d6697-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d6697-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d6697-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d6697-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d6697-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="d6697-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d6697-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6697-113">EXAMPLES</span></span>

### <span data-ttu-id="d6697-114">Exempel 1: ändra översikt över en integrerings konto</span><span class="sxs-lookup"><span data-stu-id="d6697-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="d6697-115">Det här kommandot ändrar mappnings konto översikten i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6697-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="d6697-116">Kommandot anger en kart definition som lagras i $MapContent-variabeln med ett föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="d6697-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="d6697-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d6697-117">Example 2</span></span>

<span data-ttu-id="d6697-118">Ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="d6697-118">Modifies an integration account map.</span></span> <span data-ttu-id="d6697-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="d6697-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="d6697-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6697-120">PARAMETERS</span></span>

### <span data-ttu-id="d6697-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="d6697-121">-ContentType</span></span>
<span data-ttu-id="d6697-122">Anger en innehålls typ för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="d6697-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="d6697-123">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="d6697-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="d6697-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6697-124">-DefaultProfile</span></span>
<span data-ttu-id="d6697-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d6697-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6697-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d6697-126">-Force</span></span>
<span data-ttu-id="d6697-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d6697-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6697-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="d6697-128">-MapDefinition</span></span>
<span data-ttu-id="d6697-129">Anger ett definitions objekt för integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="d6697-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="d6697-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="d6697-130">-MapFilePath</span></span>
<span data-ttu-id="d6697-131">Anger sökvägen till en definition för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="d6697-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="d6697-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="d6697-132">-MapName</span></span>
<span data-ttu-id="d6697-133">Anger namnet på en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="d6697-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="d6697-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="d6697-134">-MapType</span></span>
<span data-ttu-id="d6697-135">Anger typen för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="d6697-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="d6697-136">Denna cmdlet stöder XSLT som en typ av karta.</span><span class="sxs-lookup"><span data-stu-id="d6697-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="d6697-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d6697-137">-Metadata</span></span>
<span data-ttu-id="d6697-138">Anger ett metadataobjekt för kartan.</span><span class="sxs-lookup"><span data-stu-id="d6697-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="d6697-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6697-139">-Name</span></span>
<span data-ttu-id="d6697-140">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="d6697-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="d6697-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6697-141">-ResourceGroupName</span></span>
<span data-ttu-id="d6697-142">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d6697-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d6697-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6697-143">-Confirm</span></span>
<span data-ttu-id="d6697-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6697-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6697-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6697-145">-WhatIf</span></span>
<span data-ttu-id="d6697-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6697-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6697-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6697-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6697-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6697-148">CommonParameters</span></span>
<span data-ttu-id="d6697-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6697-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6697-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6697-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6697-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6697-151">INPUTS</span></span>

### <span data-ttu-id="d6697-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d6697-152">System.String</span></span>

## <span data-ttu-id="d6697-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6697-153">OUTPUTS</span></span>

### <span data-ttu-id="d6697-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d6697-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="d6697-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6697-155">NOTES</span></span>

## <span data-ttu-id="d6697-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6697-156">RELATED LINKS</span></span>

[<span data-ttu-id="d6697-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d6697-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="d6697-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d6697-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="d6697-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d6697-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


