---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 19f6884e9359612eab1d22018a7ebc1295f81210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584972"
---
# <span data-ttu-id="699e5-101">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="699e5-101">New-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="699e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="699e5-102">SYNOPSIS</span></span>
<span data-ttu-id="699e5-103">Skapar ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-103">Creates an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="699e5-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="699e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="699e5-105">DESCRIPTION</span></span>
<span data-ttu-id="699e5-106">Cmdleten **New-AzureRmIntegrationAccountSchema** skapar ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-106">The **New-AzureRmIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="699e5-107">Denna cmdlet returnerar ett objekt som representerar integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="699e5-108">Ange integrerings konto namn, resurs grupps namn, schema namn och schema definition.</span><span class="sxs-lookup"><span data-stu-id="699e5-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="699e5-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="699e5-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="699e5-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="699e5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="699e5-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="699e5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="699e5-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="699e5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="699e5-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="699e5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="699e5-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="699e5-114">EXAMPLES</span></span>

### <span data-ttu-id="699e5-115">Exempel 1: skapa ett integrerings konto schema</span><span class="sxs-lookup"><span data-stu-id="699e5-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="699e5-116">Det här kommandot skapar integrerings kontots schema med namnet IntegrationAccountSchema1 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="699e5-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="699e5-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="699e5-117">PARAMETERS</span></span>

### <span data-ttu-id="699e5-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="699e5-118">-ContentType</span></span>
<span data-ttu-id="699e5-119">Anger en innehålls typ för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="699e5-120">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="699e5-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="699e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699e5-121">-DefaultProfile</span></span>
<span data-ttu-id="699e5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="699e5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="699e5-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="699e5-123">-Metadata</span></span>
<span data-ttu-id="699e5-124">Anger ett metadataobjekt för schemat.</span><span class="sxs-lookup"><span data-stu-id="699e5-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="699e5-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="699e5-125">-Name</span></span>
<span data-ttu-id="699e5-126">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="699e5-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="699e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="699e5-128">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="699e5-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="699e5-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="699e5-129">-SchemaDefinition</span></span>
<span data-ttu-id="699e5-130">Anger ett definitions objekt för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="699e5-131">Ange antingen den här parametern eller parametern *SchemaFilePath* .</span><span class="sxs-lookup"><span data-stu-id="699e5-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="699e5-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="699e5-132">-SchemaFilePath</span></span>
<span data-ttu-id="699e5-133">Anger sökvägen till en definition för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="699e5-134">Ange antingen den här parametern eller parametern *SchemaDefinition* .</span><span class="sxs-lookup"><span data-stu-id="699e5-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="699e5-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="699e5-135">-SchemaName</span></span>
<span data-ttu-id="699e5-136">Anger ett namn på integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="699e5-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="699e5-137">-SchemaType</span></span>
<span data-ttu-id="699e5-138">Anger typen för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="699e5-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="699e5-139">Den här parametern har stöd för XML som typ.</span><span class="sxs-lookup"><span data-stu-id="699e5-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="699e5-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="699e5-140">-Confirm</span></span>
<span data-ttu-id="699e5-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="699e5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="699e5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699e5-142">-WhatIf</span></span>
<span data-ttu-id="699e5-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="699e5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="699e5-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="699e5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="699e5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699e5-145">CommonParameters</span></span>
<span data-ttu-id="699e5-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699e5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699e5-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699e5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699e5-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="699e5-148">INPUTS</span></span>

### <span data-ttu-id="699e5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="699e5-149">System.String</span></span>

## <span data-ttu-id="699e5-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="699e5-150">OUTPUTS</span></span>

### <span data-ttu-id="699e5-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="699e5-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="699e5-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="699e5-152">NOTES</span></span>

## <span data-ttu-id="699e5-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="699e5-153">RELATED LINKS</span></span>

[<span data-ttu-id="699e5-154">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="699e5-154">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="699e5-155">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="699e5-155">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="699e5-156">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="699e5-156">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


