---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 8887cdf7da3b69d826bedd4f6de97a8cf39d4a6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089590"
---
# <span data-ttu-id="fbe3e-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe3e-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="fbe3e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbe3e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe3e-103">Skapar ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="fbe3e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbe3e-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe3e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbe3e-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe3e-106">Cmdleten **New-AzIntegrationAccountSchema** skapar ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="fbe3e-107">Denna cmdlet returnerar ett objekt som representerar integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="fbe3e-108">Ange integrerings konto namn, resurs grupps namn, schema namn och schema definition.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="fbe3e-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="fbe3e-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fbe3e-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fbe3e-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fbe3e-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fbe3e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbe3e-114">EXAMPLES</span></span>

### <span data-ttu-id="fbe3e-115">Exempel 1: skapa ett integrerings konto schema</span><span class="sxs-lookup"><span data-stu-id="fbe3e-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="fbe3e-116">Det här kommandot skapar integrerings kontots schema med namnet IntegrationAccountSchema1 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="fbe3e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbe3e-117">PARAMETERS</span></span>

### <span data-ttu-id="fbe3e-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="fbe3e-118">-ContentType</span></span>
<span data-ttu-id="fbe3e-119">Anger en innehålls typ för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="fbe3e-120">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="fbe3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe3e-121">-DefaultProfile</span></span>
<span data-ttu-id="fbe3e-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fbe3e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe3e-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fbe3e-123">-Metadata</span></span>
<span data-ttu-id="fbe3e-124">Anger ett metadataobjekt för schemat.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="fbe3e-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbe3e-125">-Name</span></span>
<span data-ttu-id="fbe3e-126">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="fbe3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="fbe3e-128">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fbe3e-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="fbe3e-129">-SchemaDefinition</span></span>
<span data-ttu-id="fbe3e-130">Anger ett definitions objekt för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="fbe3e-131">Ange antingen den här parametern eller parametern *SchemaFilePath* .</span><span class="sxs-lookup"><span data-stu-id="fbe3e-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="fbe3e-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="fbe3e-132">-SchemaFilePath</span></span>
<span data-ttu-id="fbe3e-133">Anger sökvägen till en definition för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="fbe3e-134">Ange antingen den här parametern eller parametern *SchemaDefinition* .</span><span class="sxs-lookup"><span data-stu-id="fbe3e-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="fbe3e-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fbe3e-135">-SchemaName</span></span>
<span data-ttu-id="fbe3e-136">Anger ett namn på integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="fbe3e-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="fbe3e-137">-SchemaType</span></span>
<span data-ttu-id="fbe3e-138">Anger typen för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="fbe3e-139">Den här parametern har stöd för XML som typ.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="fbe3e-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fbe3e-140">-Confirm</span></span>
<span data-ttu-id="fbe3e-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe3e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe3e-142">-WhatIf</span></span>
<span data-ttu-id="fbe3e-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe3e-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe3e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe3e-145">CommonParameters</span></span>
<span data-ttu-id="fbe3e-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe3e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe3e-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe3e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe3e-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbe3e-148">INPUTS</span></span>

### <span data-ttu-id="fbe3e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fbe3e-149">System.String</span></span>

## <span data-ttu-id="fbe3e-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbe3e-150">OUTPUTS</span></span>

### <span data-ttu-id="fbe3e-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe3e-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="fbe3e-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbe3e-152">NOTES</span></span>

## <span data-ttu-id="fbe3e-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbe3e-153">RELATED LINKS</span></span>

[<span data-ttu-id="fbe3e-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe3e-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="fbe3e-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe3e-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="fbe3e-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="fbe3e-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


