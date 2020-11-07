---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923377"
---
# <span data-ttu-id="65300-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65300-101">Get-AzWebApp</span></span>

## <span data-ttu-id="65300-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65300-102">SYNOPSIS</span></span>
<span data-ttu-id="65300-103">Hämtar Azure Web Apps i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="65300-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="65300-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65300-104">SYNTAX</span></span>

### <span data-ttu-id="65300-105">S</span><span class="sxs-lookup"><span data-stu-id="65300-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65300-106">S2</span><span class="sxs-lookup"><span data-stu-id="65300-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65300-107">S3</span><span class="sxs-lookup"><span data-stu-id="65300-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65300-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65300-108">DESCRIPTION</span></span>
<span data-ttu-id="65300-109">Cmdleten **Get-AzWebApp** hämtar information om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="65300-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="65300-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65300-110">EXAMPLES</span></span>

### <span data-ttu-id="65300-111">Exempel 1: Hämta ett webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="65300-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="65300-112">Det här kommandot hämtar webb programmet som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="65300-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="65300-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65300-113">PARAMETERS</span></span>

### <span data-ttu-id="65300-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="65300-114">-AppServicePlan</span></span>
<span data-ttu-id="65300-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="65300-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65300-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65300-116">-DefaultProfile</span></span>
<span data-ttu-id="65300-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65300-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65300-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="65300-118">-Location</span></span>
<span data-ttu-id="65300-119">Plats</span><span class="sxs-lookup"><span data-stu-id="65300-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65300-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="65300-120">-Name</span></span>
<span data-ttu-id="65300-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="65300-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65300-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65300-122">-ResourceGroupName</span></span>
<span data-ttu-id="65300-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="65300-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65300-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65300-124">CommonParameters</span></span>
<span data-ttu-id="65300-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65300-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65300-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65300-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65300-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65300-127">INPUTS</span></span>

### <span data-ttu-id="65300-128">System. String</span><span class="sxs-lookup"><span data-stu-id="65300-128">System.String</span></span>

## <span data-ttu-id="65300-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65300-129">OUTPUTS</span></span>

### <span data-ttu-id="65300-130">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="65300-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="65300-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65300-131">NOTES</span></span>

## <span data-ttu-id="65300-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65300-132">RELATED LINKS</span></span>

[<span data-ttu-id="65300-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65300-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="65300-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65300-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="65300-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65300-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="65300-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65300-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="65300-137">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65300-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


