---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae03fd4dedf1e0e6de91bd036180379c2be2cabe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575749"
---
# <span data-ttu-id="ced60-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ced60-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="ced60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ced60-102">SYNOPSIS</span></span>
<span data-ttu-id="ced60-103">Hämtar ett Azure Web App-certifikat för SSL-bindning.</span><span class="sxs-lookup"><span data-stu-id="ced60-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ced60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ced60-104">SYNTAX</span></span>

### <span data-ttu-id="ced60-105">S</span><span class="sxs-lookup"><span data-stu-id="ced60-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ced60-106">S2</span><span class="sxs-lookup"><span data-stu-id="ced60-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ced60-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ced60-107">DESCRIPTION</span></span>
<span data-ttu-id="ced60-108">Cmdleten **Get-AzureRmWebAppSSLBinding** får en SSL-bindning (Secure Sockets Layer) för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ced60-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="ced60-109">SSL-bindningar används för att koppla ett webb program till ett uppladdat certifikat.</span><span class="sxs-lookup"><span data-stu-id="ced60-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="ced60-110">Webb program kan bindas till flera certifikat.</span><span class="sxs-lookup"><span data-stu-id="ced60-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="ced60-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ced60-111">EXAMPLES</span></span>

### <span data-ttu-id="ced60-112">Exempel 1: Hämta SSL-bindningar för ett webb program</span><span class="sxs-lookup"><span data-stu-id="ced60-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="ced60-113">Det här kommandot hämtar SSL-bindningarna för Web App-ContosoWebApp, som är kopplat till resurs gruppen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ced60-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="ced60-114">Exempel 2: använda en objekt referens för att få SSL-bindningar för ett webb program</span><span class="sxs-lookup"><span data-stu-id="ced60-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="ced60-115">Kommandona i det här exemplet hämtar också SSL-bindningarna för Web App-ContosoWebApp; i det här fallet används en objekt referens i stället för namnet på den associerade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ced60-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="ced60-116">Den här objekt referensen skapas av det första kommandot i exemplet, som använder funktionen **Get-AzureRmWebApp** för att skapa en objekt referens till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="ced60-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="ced60-117">Objekt referensen lagras i en variabel som heter $WebApp.</span><span class="sxs-lookup"><span data-stu-id="ced60-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="ced60-118">Den här variabeln och cmdleten **Get-AzureRmWebAppSSLBinding** används sedan av det andra kommandot för att hämta SSL-bindningarna.</span><span class="sxs-lookup"><span data-stu-id="ced60-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="ced60-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ced60-119">PARAMETERS</span></span>

### <span data-ttu-id="ced60-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ced60-120">-Name</span></span>
<span data-ttu-id="ced60-121">Anger namnet på SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="ced60-121">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="ced60-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced60-122">-ResourceGroupName</span></span>
<span data-ttu-id="ced60-123">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="ced60-123">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="ced60-124">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ced60-124">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="ced60-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="ced60-125">-Slot</span></span>
<span data-ttu-id="ced60-126">Anger en distributions plats för webbprogram.</span><span class="sxs-lookup"><span data-stu-id="ced60-126">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="ced60-127">Använd Get-AzureRMWebAppSlot cmdlet för att få en distributions plats.</span><span class="sxs-lookup"><span data-stu-id="ced60-127">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="ced60-128">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ced60-128">-WebApp</span></span>
<span data-ttu-id="ced60-129">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="ced60-129">Specifies a Web App.</span></span>
<span data-ttu-id="ced60-130">Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced60-130">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

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

### <span data-ttu-id="ced60-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="ced60-131">-WebAppName</span></span>
<span data-ttu-id="ced60-132">Anger namnet på den webbapp som den här cmdleten får SSL-bindningar från.</span><span class="sxs-lookup"><span data-stu-id="ced60-132">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="ced60-133">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ced60-133">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="ced60-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced60-134">-DefaultProfile</span></span>
<span data-ttu-id="ced60-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ced60-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced60-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced60-136">CommonParameters</span></span>
<span data-ttu-id="ced60-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced60-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced60-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced60-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced60-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ced60-139">INPUTS</span></span>

### <span data-ttu-id="ced60-140">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="ced60-140">Site</span></span>
<span data-ttu-id="ced60-141">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ced60-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ced60-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ced60-142">OUTPUTS</span></span>

## <span data-ttu-id="ced60-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ced60-143">NOTES</span></span>

## <span data-ttu-id="ced60-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ced60-144">RELATED LINKS</span></span>

[<span data-ttu-id="ced60-145">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ced60-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="ced60-146">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ced60-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="ced60-147">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ced60-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


