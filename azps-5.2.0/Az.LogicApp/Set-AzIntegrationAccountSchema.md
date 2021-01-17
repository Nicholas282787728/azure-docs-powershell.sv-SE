---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415552"
---
# <span data-ttu-id="dff78-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dff78-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="dff78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dff78-102">SYNOPSIS</span></span>
<span data-ttu-id="dff78-103">Ändrar ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="dff78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dff78-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dff78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dff78-105">DESCRIPTION</span></span>
<span data-ttu-id="dff78-106">Cmdleten **set-AzIntegrationAccountSchema** ändrar ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="dff78-107">Denna cmdlet returnerar ett objekt som representerar integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="dff78-108">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="dff78-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="dff78-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="dff78-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="dff78-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="dff78-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dff78-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="dff78-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dff78-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="dff78-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dff78-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="dff78-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dff78-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dff78-114">EXAMPLES</span></span>

### <span data-ttu-id="dff78-115">Exempel 1: ändra ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="dff78-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="dff78-116">Det här kommandot ändrar det integrerings konto schema som heter IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="dff78-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="dff78-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dff78-117">PARAMETERS</span></span>

### <span data-ttu-id="dff78-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="dff78-118">-ContentType</span></span>
<span data-ttu-id="dff78-119">Anger en innehålls typ för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="dff78-120">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="dff78-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="dff78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff78-121">-DefaultProfile</span></span>
<span data-ttu-id="dff78-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dff78-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dff78-123">-Force</span><span class="sxs-lookup"><span data-stu-id="dff78-123">-Force</span></span>
<span data-ttu-id="dff78-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dff78-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dff78-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dff78-125">-Metadata</span></span>
<span data-ttu-id="dff78-126">Anger ett metadataobjekt för schemat.</span><span class="sxs-lookup"><span data-stu-id="dff78-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="dff78-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="dff78-127">-Name</span></span>
<span data-ttu-id="dff78-128">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="dff78-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="dff78-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff78-129">-ResourceGroupName</span></span>
<span data-ttu-id="dff78-130">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dff78-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dff78-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="dff78-131">-SchemaDefinition</span></span>
<span data-ttu-id="dff78-132">Anger ett definitions objekt för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="dff78-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="dff78-133">-SchemaFilePath</span></span>
<span data-ttu-id="dff78-134">Anger sökvägen till en definition för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="dff78-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dff78-135">-SchemaName</span></span>
<span data-ttu-id="dff78-136">Anger namnet på integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="dff78-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="dff78-137">-SchemaType</span></span>
<span data-ttu-id="dff78-138">Anger typen för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="dff78-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="dff78-139">Den här parametern har stöd för XML som typ.</span><span class="sxs-lookup"><span data-stu-id="dff78-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dff78-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dff78-140">-Confirm</span></span>
<span data-ttu-id="dff78-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dff78-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff78-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff78-142">-WhatIf</span></span>
<span data-ttu-id="dff78-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dff78-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff78-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dff78-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff78-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff78-145">CommonParameters</span></span>
<span data-ttu-id="dff78-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff78-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff78-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff78-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff78-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dff78-148">INPUTS</span></span>

### <span data-ttu-id="dff78-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dff78-149">System.String</span></span>

## <span data-ttu-id="dff78-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dff78-150">OUTPUTS</span></span>

### <span data-ttu-id="dff78-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dff78-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="dff78-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dff78-152">NOTES</span></span>

## <span data-ttu-id="dff78-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dff78-153">RELATED LINKS</span></span>

[<span data-ttu-id="dff78-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dff78-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="dff78-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dff78-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="dff78-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dff78-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


