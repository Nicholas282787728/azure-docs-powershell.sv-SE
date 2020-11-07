---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923353"
---
# <span data-ttu-id="856a4-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="856a4-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="856a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="856a4-102">SYNOPSIS</span></span>
<span data-ttu-id="856a4-103">Hämtar ett Azure Web App-certifikat för SSL-bindning.</span><span class="sxs-lookup"><span data-stu-id="856a4-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="856a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="856a4-104">SYNTAX</span></span>

### <span data-ttu-id="856a4-105">S</span><span class="sxs-lookup"><span data-stu-id="856a4-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="856a4-106">S2</span><span class="sxs-lookup"><span data-stu-id="856a4-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="856a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="856a4-107">DESCRIPTION</span></span>
<span data-ttu-id="856a4-108">Cmdleten **Get-AzWebAppSSLBinding** får en SSL-bindning (Secure Sockets Layer) för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="856a4-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="856a4-109">SSL-bindningar används för att koppla ett webb program till ett uppladdat certifikat.</span><span class="sxs-lookup"><span data-stu-id="856a4-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="856a4-110">Webb program kan bindas till flera certifikat.</span><span class="sxs-lookup"><span data-stu-id="856a4-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="856a4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="856a4-111">EXAMPLES</span></span>

### <span data-ttu-id="856a4-112">Exempel 1: Hämta SSL-bindningar för ett webb program</span><span class="sxs-lookup"><span data-stu-id="856a4-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="856a4-113">Det här kommandot hämtar SSL-bindningarna för Web App-ContosoWebApp, som är kopplat till resurs gruppen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="856a4-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="856a4-114">Exempel 2: använda en objekt referens för att få SSL-bindningar för ett webb program</span><span class="sxs-lookup"><span data-stu-id="856a4-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="856a4-115">Kommandona i det här exemplet hämtar också SSL-bindningarna för Web App-ContosoWebApp; i det här fallet används en objekt referens i stället för namnet på den associerade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="856a4-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="856a4-116">Den här objekt referensen skapas av det första kommandot i exemplet, som använder funktionen **Get-AzWebApp** för att skapa en objekt referens till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="856a4-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="856a4-117">Objekt referensen lagras i en variabel som heter $WebApp.</span><span class="sxs-lookup"><span data-stu-id="856a4-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="856a4-118">Den här variabeln och cmdleten **Get-AzWebAppSSLBinding** används sedan av det andra kommandot för att hämta SSL-bindningarna.</span><span class="sxs-lookup"><span data-stu-id="856a4-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="856a4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="856a4-119">PARAMETERS</span></span>

### <span data-ttu-id="856a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856a4-120">-DefaultProfile</span></span>
<span data-ttu-id="856a4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="856a4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="856a4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="856a4-122">-Name</span></span>
<span data-ttu-id="856a4-123">Anger namnet på SSL-bindningen.</span><span class="sxs-lookup"><span data-stu-id="856a4-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="856a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="856a4-125">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="856a4-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="856a4-126">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="856a4-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="856a4-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="856a4-127">-Slot</span></span>
<span data-ttu-id="856a4-128">Anger en distributions plats för webbprogram.</span><span class="sxs-lookup"><span data-stu-id="856a4-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="856a4-129">Använd Get-AzWebAppSlot cmdlet för att få en distributions plats.</span><span class="sxs-lookup"><span data-stu-id="856a4-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="856a4-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="856a4-130">-WebApp</span></span>
<span data-ttu-id="856a4-131">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="856a4-131">Specifies a Web App.</span></span>
<span data-ttu-id="856a4-132">Om du vill hämta en webbapp använder du Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="856a4-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="856a4-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="856a4-133">-WebAppName</span></span>
<span data-ttu-id="856a4-134">Anger namnet på den webbapp som den här cmdleten får SSL-bindningar från.</span><span class="sxs-lookup"><span data-stu-id="856a4-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="856a4-135">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="856a4-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="856a4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856a4-136">CommonParameters</span></span>
<span data-ttu-id="856a4-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856a4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856a4-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856a4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856a4-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="856a4-139">INPUTS</span></span>

### <span data-ttu-id="856a4-140">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="856a4-140">Site</span></span>
<span data-ttu-id="856a4-141">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="856a4-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="856a4-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="856a4-142">OUTPUTS</span></span>

## <span data-ttu-id="856a4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="856a4-143">NOTES</span></span>

## <span data-ttu-id="856a4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="856a4-144">RELATED LINKS</span></span>

[<span data-ttu-id="856a4-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="856a4-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="856a4-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="856a4-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="856a4-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="856a4-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


