---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 553a9561939ffcef3337b0c13d384c5f5f47340e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757973"
---
# <span data-ttu-id="f9734-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f9734-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="f9734-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9734-102">SYNOPSIS</span></span>
<span data-ttu-id="f9734-103">Tar bort en SSL-bindning från ett uppladdat certifikat.</span><span class="sxs-lookup"><span data-stu-id="f9734-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9734-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9734-104">SYNTAX</span></span>

### <span data-ttu-id="f9734-105">S</span><span class="sxs-lookup"><span data-stu-id="f9734-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9734-106">S2</span><span class="sxs-lookup"><span data-stu-id="f9734-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9734-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9734-107">DESCRIPTION</span></span>
<span data-ttu-id="f9734-108">Cmdleten **Remove-AzureRmWebAppSSLBinding** tar bort en SSL-bindning från en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f9734-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="f9734-109">SSL-bindningar används för att koppla ett webb program till ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="f9734-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="f9734-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9734-110">EXAMPLES</span></span>

### <span data-ttu-id="f9734-111">Exempel 1: ta bort en SSL-bindning för ett webb program</span><span class="sxs-lookup"><span data-stu-id="f9734-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="f9734-112">Det här kommandot tar bort SSL-bindningen för webb programmet ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f9734-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="f9734-113">Eftersom parametern *DeleteCertificate* inte är inkluderad tas certifikatet bort om det inte längre har några SSL-bindningar.</span><span class="sxs-lookup"><span data-stu-id="f9734-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="f9734-114">Exempel 2: ta bort en SSL-bindning utan att ta bort certifikatet</span><span class="sxs-lookup"><span data-stu-id="f9734-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="f9734-115">Precis som i exempel 1 tar det här kommandot också bort SSL-bindningen för Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f9734-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="f9734-116">I det här fallet är parametern *DeleteCertificate* inkluderad och parametervärdet är inställt på $false.</span><span class="sxs-lookup"><span data-stu-id="f9734-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="f9734-117">Det innebär att certifikatet inte tas bort oavsett om det har SSL-bindningar eller inte.</span><span class="sxs-lookup"><span data-stu-id="f9734-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="f9734-118">Exempel 3: använda en objekt referens för att ta bort en SSL-bindning</span><span class="sxs-lookup"><span data-stu-id="f9734-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="f9734-119">I det här exemplet används en objekt referens till Web App-webbplatsen för att ta bort SSL-bindningen för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="f9734-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="f9734-120">Det första kommandot använder cmdleten Get-AzureRmWebApp för att skapa en objekt referens till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f9734-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="f9734-121">Objekt referensen lagras i en variabel som heter $WebApp.</span><span class="sxs-lookup"><span data-stu-id="f9734-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="f9734-122">Det andra kommandot använder objekt referensen och cmdleten **Remove-AzureRmWebAppSSLBinding** för att ta bort SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="f9734-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="f9734-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9734-123">PARAMETERS</span></span>

### <span data-ttu-id="f9734-124">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="f9734-124">-DeleteCertificate</span></span>
<span data-ttu-id="f9734-125">Anger vilken åtgärd som ska vidtas om SSL-bindningen som tas bort är den enda bindning som används av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f9734-125">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="f9734-126">Om *DeleteCertificate* är inställt på $false tas certifikatet inte bort när bindningen tas bort.</span><span class="sxs-lookup"><span data-stu-id="f9734-126">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="f9734-127">Om *DeleteCertificate* är inställt på $True eller inte ingår i kommandot tas certifikatet bort tillsammans med SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="f9734-127">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="f9734-128">Certifikatet tas bara bort om den SSL-bindning som tas bort är den enda bindning som används av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="f9734-128">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="f9734-129">Om certifikatet har mer än en bindning tas certifikatet inte bort oavsett värdet på parametern *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="f9734-129">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f9734-130">-Force</span></span>
<span data-ttu-id="f9734-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f9734-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9734-132">-Name</span></span>
<span data-ttu-id="f9734-133">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="f9734-133">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9734-134">-ResourceGroupName</span></span>
<span data-ttu-id="f9734-135">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="f9734-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="f9734-136">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="f9734-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="f9734-137">-Slot</span></span>
<span data-ttu-id="f9734-138">Anger webb programmets distributions plats.</span><span class="sxs-lookup"><span data-stu-id="f9734-138">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="f9734-139">Använd Get-AzureRMWebAppSlot cmdlet för att få en distributions plats.</span><span class="sxs-lookup"><span data-stu-id="f9734-139">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-140">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f9734-140">-WebApp</span></span>
<span data-ttu-id="f9734-141">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="f9734-141">Specifies a Web App.</span></span>
<span data-ttu-id="f9734-142">Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9734-142">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="f9734-143">Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="f9734-143">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-144">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f9734-144">-WebAppName</span></span>
<span data-ttu-id="f9734-145">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="f9734-145">Specifies the name of the Web App.</span></span>

<span data-ttu-id="f9734-146">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="f9734-146">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9734-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9734-147">-Confirm</span></span>
<span data-ttu-id="f9734-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9734-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9734-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9734-149">-WhatIf</span></span>
<span data-ttu-id="f9734-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9734-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9734-151">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9734-151">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9734-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9734-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9734-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9734-153">-DefaultProfile</span></span>
<span data-ttu-id="f9734-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9734-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9734-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9734-155">CommonParameters</span></span>
<span data-ttu-id="f9734-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9734-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9734-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9734-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9734-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9734-158">INPUTS</span></span>

### <span data-ttu-id="f9734-159">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="f9734-159">Site</span></span>
<span data-ttu-id="f9734-160">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f9734-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f9734-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9734-161">OUTPUTS</span></span>

## <span data-ttu-id="f9734-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9734-162">NOTES</span></span>

## <span data-ttu-id="f9734-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9734-163">RELATED LINKS</span></span>

[<span data-ttu-id="f9734-164">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f9734-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f9734-165">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f9734-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f9734-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f9734-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="f9734-167">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f9734-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


