---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: cff96908b0a20cd9cb63a45781e73fb12c0a8bd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916034"
---
# <span data-ttu-id="feb05-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="feb05-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="feb05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="feb05-102">SYNOPSIS</span></span>
<span data-ttu-id="feb05-103">Skapar en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="feb05-103">Creates an integration account map.</span></span>

## <span data-ttu-id="feb05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="feb05-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="feb05-105">DESCRIPTION</span></span>
<span data-ttu-id="feb05-106">Cmdleten **New-AzIntegrationAccountMap** skapar en översikt över integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="feb05-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="feb05-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="feb05-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="feb05-108">Ange integrerings konto namnet, resurs gruppens namn, mappningens namn och kart definitionen.</span><span class="sxs-lookup"><span data-stu-id="feb05-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="feb05-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="feb05-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="feb05-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="feb05-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="feb05-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="feb05-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="feb05-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="feb05-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="feb05-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="feb05-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="feb05-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="feb05-114">EXAMPLES</span></span>

### <span data-ttu-id="feb05-115">Exempel 1: skapa en integrerings konto karta</span><span class="sxs-lookup"><span data-stu-id="feb05-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="feb05-116">Det här kommandot skapar integrerings konto översikten i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="feb05-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="feb05-117">Kommandot anger en kart definition som lagras i $MapContent-variabeln med ett föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="feb05-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="feb05-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="feb05-118">PARAMETERS</span></span>

### <span data-ttu-id="feb05-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="feb05-119">-ContentType</span></span>
<span data-ttu-id="feb05-120">Anger en innehålls typ för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="feb05-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="feb05-121">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="feb05-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="feb05-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb05-122">-DefaultProfile</span></span>
<span data-ttu-id="feb05-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="feb05-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="feb05-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="feb05-124">-MapDefinition</span></span>
<span data-ttu-id="feb05-125">Anger ett definitions objekt för integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="feb05-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="feb05-126">Ange antingen den här parametern eller parametern *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="feb05-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="feb05-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="feb05-127">-MapFilePath</span></span>
<span data-ttu-id="feb05-128">Anger sökvägen till en definition för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="feb05-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="feb05-129">Ange antingen den här parametern eller parametern *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="feb05-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="feb05-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="feb05-130">-MapName</span></span>
<span data-ttu-id="feb05-131">Anger ett namn för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="feb05-131">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="feb05-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="feb05-132">-MapType</span></span>
<span data-ttu-id="feb05-133">Anger typen för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="feb05-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="feb05-134">Denna cmdlet stöder XSLT som en typ av karta.</span><span class="sxs-lookup"><span data-stu-id="feb05-134">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="feb05-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="feb05-135">-Metadata</span></span>
<span data-ttu-id="feb05-136">Anger ett metadataobjekt för kartan.</span><span class="sxs-lookup"><span data-stu-id="feb05-136">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="feb05-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="feb05-137">-Name</span></span>
<span data-ttu-id="feb05-138">Anger ett namn på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="feb05-138">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="feb05-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb05-139">-ResourceGroupName</span></span>
<span data-ttu-id="feb05-140">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="feb05-140">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="feb05-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="feb05-141">-Confirm</span></span>
<span data-ttu-id="feb05-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="feb05-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb05-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb05-143">-WhatIf</span></span>
<span data-ttu-id="feb05-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="feb05-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb05-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="feb05-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb05-146">CommonParameters</span></span>
<span data-ttu-id="feb05-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb05-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb05-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb05-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="feb05-149">INPUTS</span></span>

### <span data-ttu-id="feb05-150">System. String</span><span class="sxs-lookup"><span data-stu-id="feb05-150">System.String</span></span>

## <span data-ttu-id="feb05-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="feb05-151">OUTPUTS</span></span>

### <span data-ttu-id="feb05-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="feb05-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="feb05-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="feb05-153">NOTES</span></span>

## <span data-ttu-id="feb05-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="feb05-154">RELATED LINKS</span></span>

[<span data-ttu-id="feb05-155">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="feb05-155">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="feb05-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="feb05-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="feb05-157">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="feb05-157">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


