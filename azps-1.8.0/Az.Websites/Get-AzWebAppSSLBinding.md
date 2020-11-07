---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: a50716315796d46185b67099784bc550295231e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746076"
---
# <span data-ttu-id="72c01-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="72c01-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="72c01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72c01-102">SYNOPSIS</span></span>
<span data-ttu-id="72c01-103">Hämtar ett Azure Web App-certifikat för SSL-bindning.</span><span class="sxs-lookup"><span data-stu-id="72c01-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="72c01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72c01-104">SYNTAX</span></span>

### <span data-ttu-id="72c01-105">S</span><span class="sxs-lookup"><span data-stu-id="72c01-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72c01-106">S2</span><span class="sxs-lookup"><span data-stu-id="72c01-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72c01-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72c01-107">DESCRIPTION</span></span>
<span data-ttu-id="72c01-108">Cmdleten **Get-AzWebAppSSLBinding** får en SSL-bindning (Secure Sockets Layer) för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="72c01-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="72c01-109">SSL-bindningar används för att koppla ett webb program till ett uppladdat certifikat.</span><span class="sxs-lookup"><span data-stu-id="72c01-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="72c01-110">Webb program kan bindas till flera certifikat.</span><span class="sxs-lookup"><span data-stu-id="72c01-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="72c01-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72c01-111">EXAMPLES</span></span>

### <span data-ttu-id="72c01-112">Exempel 1: Hämta SSL-bindningar för ett webb program</span><span class="sxs-lookup"><span data-stu-id="72c01-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="72c01-113">Det här kommandot hämtar SSL-bindningarna för Web App-ContosoWebApp, som är kopplat till resurs gruppen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="72c01-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="72c01-114">Exempel 2: använda en objekt referens för att få SSL-bindningar för ett webb program</span><span class="sxs-lookup"><span data-stu-id="72c01-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="72c01-115">Kommandona i det här exemplet hämtar också SSL-bindningarna för Web App-ContosoWebApp; i det här fallet används en objekt referens i stället för namnet på den associerade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72c01-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="72c01-116">Den här objekt referensen skapas av det första kommandot i exemplet, som använder funktionen **Get-AzWebApp** för att skapa en objekt referens till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="72c01-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="72c01-117">Objekt referensen lagras i en variabel som heter $WebApp.</span><span class="sxs-lookup"><span data-stu-id="72c01-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="72c01-118">Den här variabeln och cmdleten **Get-AzWebAppSSLBinding** används sedan av det andra kommandot för att hämta SSL-bindningarna.</span><span class="sxs-lookup"><span data-stu-id="72c01-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="72c01-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72c01-119">PARAMETERS</span></span>

### <span data-ttu-id="72c01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c01-120">-DefaultProfile</span></span>
<span data-ttu-id="72c01-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72c01-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72c01-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="72c01-122">-Name</span></span>
<span data-ttu-id="72c01-123">Anger namnet på SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="72c01-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c01-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c01-124">-ResourceGroupName</span></span>
<span data-ttu-id="72c01-125">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="72c01-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="72c01-126">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="72c01-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="72c01-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="72c01-127">-Slot</span></span>
<span data-ttu-id="72c01-128">Anger en distributions plats för webbprogram.</span><span class="sxs-lookup"><span data-stu-id="72c01-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="72c01-129">Använd Get-AzWebAppSlot cmdlet för att få en distributions plats.</span><span class="sxs-lookup"><span data-stu-id="72c01-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="72c01-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="72c01-130">-WebApp</span></span>
<span data-ttu-id="72c01-131">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="72c01-131">Specifies a Web App.</span></span>
<span data-ttu-id="72c01-132">Om du vill hämta en webbapp använder du Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72c01-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72c01-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="72c01-133">-WebAppName</span></span>
<span data-ttu-id="72c01-134">Anger namnet på den webbapp som den här cmdleten får SSL-bindningar från.</span><span class="sxs-lookup"><span data-stu-id="72c01-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="72c01-135">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="72c01-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="72c01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c01-136">CommonParameters</span></span>
<span data-ttu-id="72c01-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c01-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c01-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c01-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72c01-139">INPUTS</span></span>

### <span data-ttu-id="72c01-140">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="72c01-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="72c01-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72c01-141">OUTPUTS</span></span>

### <span data-ttu-id="72c01-142">Microsoft. Azure. Management. webbplatser. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="72c01-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="72c01-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72c01-143">NOTES</span></span>

## <span data-ttu-id="72c01-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72c01-144">RELATED LINKS</span></span>

[<span data-ttu-id="72c01-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="72c01-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="72c01-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="72c01-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="72c01-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="72c01-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


