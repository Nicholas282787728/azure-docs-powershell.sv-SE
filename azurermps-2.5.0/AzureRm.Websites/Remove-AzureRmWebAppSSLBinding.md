---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 06bb13207a666b4537c267e391818865e4165e74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928633"
---
# <span data-ttu-id="64c8b-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="64c8b-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="64c8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="64c8b-103">Tar bort en SSL-bindning från ett uppladdat certifikat.</span><span class="sxs-lookup"><span data-stu-id="64c8b-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64c8b-104">SYNTAX</span></span>

### <span data-ttu-id="64c8b-105">S</span><span class="sxs-lookup"><span data-stu-id="64c8b-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64c8b-106">S2</span><span class="sxs-lookup"><span data-stu-id="64c8b-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c8b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64c8b-107">DESCRIPTION</span></span>
<span data-ttu-id="64c8b-108">Cmdleten **Remove-AzureRmWebAppSSLBinding** tar bort en SSL-bindning från en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="64c8b-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="64c8b-109">SSL-bindningar används för att koppla ett webb program till ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="64c8b-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="64c8b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64c8b-110">EXAMPLES</span></span>

### <span data-ttu-id="64c8b-111">Exempel 1: ta bort en SSL-bindning för ett webb program</span><span class="sxs-lookup"><span data-stu-id="64c8b-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="64c8b-112">Det här kommandot tar bort SSL-bindningen för webb programmet ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="64c8b-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="64c8b-113">Eftersom parametern *DeleteCertificate* inte är inkluderad tas certifikatet bort om det inte längre har några SSL-bindningar.</span><span class="sxs-lookup"><span data-stu-id="64c8b-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="64c8b-114">Exempel 2: ta bort en SSL-bindning utan att ta bort certifikatet</span><span class="sxs-lookup"><span data-stu-id="64c8b-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="64c8b-115">Precis som i exempel 1 tar det här kommandot också bort SSL-bindningen för Web App-ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="64c8b-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="64c8b-116">I det här fallet är parametern *DeleteCertificate* inkluderad och parametervärdet är inställt på $false.</span><span class="sxs-lookup"><span data-stu-id="64c8b-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="64c8b-117">Det innebär att certifikatet inte tas bort oavsett om det har SSL-bindningar eller inte.</span><span class="sxs-lookup"><span data-stu-id="64c8b-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="64c8b-118">Exempel 3: använda en objekt referens för att ta bort en SSL-bindning</span><span class="sxs-lookup"><span data-stu-id="64c8b-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="64c8b-119">I det här exemplet används en objekt referens till Web App-webbplatsen för att ta bort SSL-bindningen för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="64c8b-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="64c8b-120">Det första kommandot använder cmdleten Get-AzureRmWebApp för att skapa en objekt referens till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="64c8b-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="64c8b-121">Objekt referensen lagras i en variabel som heter $WebApp.</span><span class="sxs-lookup"><span data-stu-id="64c8b-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="64c8b-122">Det andra kommandot använder objekt referensen och cmdleten **Remove-AzureRmWebAppSSLBinding** för att ta bort SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="64c8b-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="64c8b-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64c8b-123">PARAMETERS</span></span>

### <span data-ttu-id="64c8b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c8b-124">-DefaultProfile</span></span>
<span data-ttu-id="64c8b-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64c8b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64c8b-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="64c8b-126">-DeleteCertificate</span></span>
<span data-ttu-id="64c8b-127">Anger vilken åtgärd som ska vidtas om SSL-bindningen som tas bort är den enda bindning som används av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="64c8b-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="64c8b-128">Om *DeleteCertificate* är inställt på $false tas certifikatet inte bort när bindningen tas bort.</span><span class="sxs-lookup"><span data-stu-id="64c8b-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="64c8b-129">Om *DeleteCertificate* är inställt på $True eller inte ingår i kommandot tas certifikatet bort tillsammans med SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="64c8b-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="64c8b-130">Certifikatet tas bara bort om den SSL-bindning som tas bort är den enda bindning som används av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="64c8b-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="64c8b-131">Om certifikatet har mer än en bindning tas certifikatet inte bort oavsett värdet på parametern *DeleteCertificate* .</span><span class="sxs-lookup"><span data-stu-id="64c8b-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="64c8b-132">-Force</span></span>
<span data-ttu-id="64c8b-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="64c8b-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="64c8b-134">-Name</span></span>
<span data-ttu-id="64c8b-135">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="64c8b-135">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c8b-136">-ResourceGroupName</span></span>
<span data-ttu-id="64c8b-137">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="64c8b-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="64c8b-138">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="64c8b-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="64c8b-139">-Slot</span></span>
<span data-ttu-id="64c8b-140">Anger webb programmets distributions plats.</span><span class="sxs-lookup"><span data-stu-id="64c8b-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="64c8b-141">Använd Get-AzureRMWebAppSlot cmdlet för att få en distributions plats.</span><span class="sxs-lookup"><span data-stu-id="64c8b-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="64c8b-142">-WebApp</span></span>
<span data-ttu-id="64c8b-143">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="64c8b-143">Specifies a Web App.</span></span>
<span data-ttu-id="64c8b-144">Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c8b-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="64c8b-145">Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="64c8b-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="64c8b-146">-WebAppName</span></span>
<span data-ttu-id="64c8b-147">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="64c8b-147">Specifies the name of the Web App.</span></span>

<span data-ttu-id="64c8b-148">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="64c8b-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c8b-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64c8b-149">-Confirm</span></span>
<span data-ttu-id="64c8b-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64c8b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c8b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c8b-151">-WhatIf</span></span>
<span data-ttu-id="64c8b-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64c8b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c8b-153">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64c8b-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c8b-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64c8b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c8b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c8b-155">CommonParameters</span></span>
<span data-ttu-id="64c8b-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c8b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c8b-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c8b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c8b-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64c8b-158">INPUTS</span></span>

### <span data-ttu-id="64c8b-159">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="64c8b-159">Site</span></span>
<span data-ttu-id="64c8b-160">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="64c8b-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="64c8b-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64c8b-161">OUTPUTS</span></span>

## <span data-ttu-id="64c8b-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64c8b-162">NOTES</span></span>

## <span data-ttu-id="64c8b-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64c8b-163">RELATED LINKS</span></span>

[<span data-ttu-id="64c8b-164">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="64c8b-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="64c8b-165">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="64c8b-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="64c8b-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="64c8b-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="64c8b-167">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="64c8b-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


