---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: e9981f32422f51910d7e1467f4da0b0c44118f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758225"
---
# <span data-ttu-id="a3937-101">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a3937-101">Set-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="a3937-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3937-102">SYNOPSIS</span></span>
<span data-ttu-id="a3937-103">Ändrar ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-103">Modifies an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3937-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3937-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3937-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3937-105">DESCRIPTION</span></span>
<span data-ttu-id="a3937-106">Cmdleten **set-AzureRmIntegrationAccountSchema** ändrar ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-106">The **Set-AzureRmIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="a3937-107">Denna cmdlet returnerar ett objekt som representerar integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="a3937-108">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="a3937-108">Specify the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="a3937-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="a3937-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="a3937-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="a3937-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a3937-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="a3937-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a3937-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a3937-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a3937-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="a3937-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a3937-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3937-114">EXAMPLES</span></span>

### <span data-ttu-id="a3937-115">Exempel 1: ändra ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="a3937-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="a3937-116">Det här kommandot ändrar det integrerings konto schema som heter IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="a3937-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="a3937-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3937-117">PARAMETERS</span></span>

### <span data-ttu-id="a3937-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="a3937-118">-ContentType</span></span>
<span data-ttu-id="a3937-119">Anger en innehålls typ för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="a3937-120">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="a3937-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3937-121">-DefaultProfile</span></span>
<span data-ttu-id="a3937-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a3937-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3937-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a3937-123">-Force</span></span>
<span data-ttu-id="a3937-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a3937-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a3937-125">-Metadata</span></span>
<span data-ttu-id="a3937-126">Anger ett metadataobjekt för schemat.</span><span class="sxs-lookup"><span data-stu-id="a3937-126">Specifies a metadata object for the schema.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3937-127">-Name</span></span>
<span data-ttu-id="a3937-128">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="a3937-128">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3937-129">-ResourceGroupName</span></span>
<span data-ttu-id="a3937-130">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a3937-130">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="a3937-131">-SchemaDefinition</span></span>
<span data-ttu-id="a3937-132">Anger ett definitions objekt för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-132">Specifies a definition object for integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="a3937-133">-SchemaFilePath</span></span>
<span data-ttu-id="a3937-134">Anger sökvägen till en definition för integrerings kontots schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-134">Specifies the file path of a definition for the integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a3937-135">-SchemaName</span></span>
<span data-ttu-id="a3937-136">Anger namnet på integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-136">Specifies the name of the integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="a3937-137">-SchemaType</span></span>
<span data-ttu-id="a3937-138">Anger typen för integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="a3937-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="a3937-139">Den här parametern har stöd för XML som typ.</span><span class="sxs-lookup"><span data-stu-id="a3937-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3937-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3937-140">-Confirm</span></span>
<span data-ttu-id="a3937-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3937-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3937-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3937-142">-WhatIf</span></span>
<span data-ttu-id="a3937-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3937-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3937-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3937-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3937-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3937-145">CommonParameters</span></span>
<span data-ttu-id="a3937-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3937-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3937-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3937-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3937-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3937-148">INPUTS</span></span>

### <span data-ttu-id="a3937-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3937-149">None</span></span>
<span data-ttu-id="a3937-150">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a3937-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3937-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3937-151">OUTPUTS</span></span>

### <span data-ttu-id="a3937-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a3937-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="a3937-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3937-153">NOTES</span></span>

## <span data-ttu-id="a3937-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3937-154">RELATED LINKS</span></span>

[<span data-ttu-id="a3937-155">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a3937-155">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="a3937-156">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a3937-156">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="a3937-157">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a3937-157">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

