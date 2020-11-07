---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 3e4a8a68ce6af6a8be30750d0eaf8e5393ac409f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756938"
---
# <span data-ttu-id="1f708-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1f708-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="1f708-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f708-102">SYNOPSIS</span></span>
<span data-ttu-id="1f708-103">Ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="1f708-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f708-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f708-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f708-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f708-105">DESCRIPTION</span></span>
<span data-ttu-id="1f708-106">Cmdleten **set-AzureRmIntegrationAccountMap** ändrar en integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="1f708-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="1f708-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="1f708-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="1f708-108">Ange integrerings konto namnet, resurs gruppens namn och kartans namn.</span><span class="sxs-lookup"><span data-stu-id="1f708-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="1f708-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="1f708-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1f708-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="1f708-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1f708-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="1f708-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1f708-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="1f708-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1f708-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f708-113">EXAMPLES</span></span>

### <span data-ttu-id="1f708-114">Exempel 1: ändra översikt över en integrerings konto</span><span class="sxs-lookup"><span data-stu-id="1f708-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="1f708-115">Det här kommandot ändrar mappnings konto översikten i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1f708-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="1f708-116">Kommandot anger en kart definition som lagras i $MapContent-variabeln med ett föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="1f708-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="1f708-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f708-117">PARAMETERS</span></span>

### <span data-ttu-id="1f708-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="1f708-118">-ContentType</span></span>
<span data-ttu-id="1f708-119">Anger en innehålls typ för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="1f708-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="1f708-120">Denna cmdlet har stöd för program/XML som kart innehålls typ.</span><span class="sxs-lookup"><span data-stu-id="1f708-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="1f708-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1f708-121">-Force</span></span>
<span data-ttu-id="1f708-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1f708-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f708-123">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="1f708-123">-MapDefinition</span></span>
<span data-ttu-id="1f708-124">Anger ett definitions objekt för integrations konto karta.</span><span class="sxs-lookup"><span data-stu-id="1f708-124">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="1f708-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="1f708-125">-MapFilePath</span></span>
<span data-ttu-id="1f708-126">Anger sökvägen till en definition för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="1f708-126">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="1f708-127">-MapName</span><span class="sxs-lookup"><span data-stu-id="1f708-127">-MapName</span></span>
<span data-ttu-id="1f708-128">Anger namnet på en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="1f708-128">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="1f708-129">-MapType</span><span class="sxs-lookup"><span data-stu-id="1f708-129">-MapType</span></span>
<span data-ttu-id="1f708-130">Anger typen för integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="1f708-130">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="1f708-131">Denna cmdlet stöder XSLT som en typ av karta.</span><span class="sxs-lookup"><span data-stu-id="1f708-131">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f708-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1f708-132">-Metadata</span></span>
<span data-ttu-id="1f708-133">Anger ett metadataobjekt för kartan.</span><span class="sxs-lookup"><span data-stu-id="1f708-133">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="1f708-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f708-134">-Name</span></span>
<span data-ttu-id="1f708-135">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="1f708-135">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="1f708-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f708-136">-ResourceGroupName</span></span>
<span data-ttu-id="1f708-137">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1f708-137">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1f708-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f708-138">-Confirm</span></span>
<span data-ttu-id="1f708-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f708-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f708-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f708-140">-WhatIf</span></span>
<span data-ttu-id="1f708-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f708-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f708-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f708-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f708-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f708-143">-DefaultProfile</span></span>
<span data-ttu-id="1f708-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f708-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f708-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f708-145">CommonParameters</span></span>
<span data-ttu-id="1f708-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f708-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f708-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f708-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f708-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f708-148">INPUTS</span></span>

## <span data-ttu-id="1f708-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f708-149">OUTPUTS</span></span>

### <span data-ttu-id="1f708-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1f708-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="1f708-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f708-151">NOTES</span></span>

## <span data-ttu-id="1f708-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f708-152">RELATED LINKS</span></span>

[<span data-ttu-id="1f708-153">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1f708-153">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="1f708-154">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1f708-154">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="1f708-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1f708-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


