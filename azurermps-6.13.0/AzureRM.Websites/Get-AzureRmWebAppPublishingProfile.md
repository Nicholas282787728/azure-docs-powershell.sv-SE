---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576008"
---
# <span data-ttu-id="3c63b-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="3c63b-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="3c63b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c63b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c63b-103">Hämtar en Azure Web App-publicerande profil.</span><span class="sxs-lookup"><span data-stu-id="3c63b-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c63b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c63b-104">SYNTAX</span></span>

### <span data-ttu-id="3c63b-105">S</span><span class="sxs-lookup"><span data-stu-id="3c63b-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c63b-106">S2</span><span class="sxs-lookup"><span data-stu-id="3c63b-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c63b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c63b-107">DESCRIPTION</span></span>
<span data-ttu-id="3c63b-108">Cmdleten **Get-AzureRmWebAppPublishingProfile** hämtar en Azure Web App-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="3c63b-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="3c63b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c63b-109">EXAMPLES</span></span>

### <span data-ttu-id="3c63b-110">9.1</span><span class="sxs-lookup"><span data-stu-id="3c63b-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="3c63b-111">Det här kommandot hämtar publicerings profilen i FTP-format för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="3c63b-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="3c63b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c63b-112">PARAMETERS</span></span>

### <span data-ttu-id="3c63b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c63b-113">-DefaultProfile</span></span>
<span data-ttu-id="3c63b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c63b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c63b-115">-Format</span><span class="sxs-lookup"><span data-stu-id="3c63b-115">-Format</span></span>
<span data-ttu-id="3c63b-116">Format</span><span class="sxs-lookup"><span data-stu-id="3c63b-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c63b-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="3c63b-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="3c63b-118">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="3c63b-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c63b-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c63b-119">-Name</span></span>
<span data-ttu-id="3c63b-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="3c63b-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c63b-121">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="3c63b-121">-OutputFile</span></span>
<span data-ttu-id="3c63b-122">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="3c63b-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c63b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c63b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c63b-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3c63b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3c63b-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3c63b-125">-WebApp</span></span>
<span data-ttu-id="3c63b-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="3c63b-126">WebApp Object</span></span>

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

### <span data-ttu-id="3c63b-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="3c63b-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="3c63b-128">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="3c63b-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c63b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c63b-129">CommonParameters</span></span>
<span data-ttu-id="3c63b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c63b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c63b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c63b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c63b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c63b-132">INPUTS</span></span>

### <span data-ttu-id="3c63b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3c63b-133">System.String</span></span>

### <span data-ttu-id="3c63b-134">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="3c63b-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="3c63b-135">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3c63b-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="3c63b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c63b-136">OUTPUTS</span></span>

### <span data-ttu-id="3c63b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3c63b-137">System.String</span></span>

## <span data-ttu-id="3c63b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c63b-138">NOTES</span></span>

## <span data-ttu-id="3c63b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c63b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3c63b-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3c63b-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="3c63b-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3c63b-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


