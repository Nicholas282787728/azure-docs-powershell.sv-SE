---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388074"
---
# <span data-ttu-id="73888-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="73888-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="73888-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73888-102">SYNOPSIS</span></span>
<span data-ttu-id="73888-103">Hämtar en Azure Web App-publicerande profil.</span><span class="sxs-lookup"><span data-stu-id="73888-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="73888-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73888-104">SYNTAX</span></span>

### <span data-ttu-id="73888-105">S</span><span class="sxs-lookup"><span data-stu-id="73888-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73888-106">S2</span><span class="sxs-lookup"><span data-stu-id="73888-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73888-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73888-107">DESCRIPTION</span></span>
<span data-ttu-id="73888-108">Cmdleten **Get-AzWebAppPublishingProfile** hämtar en Azure Web App-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="73888-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="73888-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73888-109">EXAMPLES</span></span>

### <span data-ttu-id="73888-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73888-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="73888-111">Det här kommandot hämtar publicerings profilen i FTP-format för Web App-ContosoWebApp som är kopplad till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="73888-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="73888-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73888-112">PARAMETERS</span></span>

### <span data-ttu-id="73888-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73888-113">-DefaultProfile</span></span>
<span data-ttu-id="73888-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73888-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73888-115">-Format</span><span class="sxs-lookup"><span data-stu-id="73888-115">-Format</span></span>
<span data-ttu-id="73888-116">Format</span><span class="sxs-lookup"><span data-stu-id="73888-116">Format</span></span>

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

### <span data-ttu-id="73888-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="73888-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="73888-118">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="73888-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="73888-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="73888-119">-Name</span></span>
<span data-ttu-id="73888-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="73888-120">WebApp Name</span></span>

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

### <span data-ttu-id="73888-121">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="73888-121">-OutputFile</span></span>
<span data-ttu-id="73888-122">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="73888-122">Output File</span></span>

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

### <span data-ttu-id="73888-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73888-123">-ResourceGroupName</span></span>
<span data-ttu-id="73888-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="73888-124">Resource Group Name</span></span>

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

### <span data-ttu-id="73888-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="73888-125">-WebApp</span></span>
<span data-ttu-id="73888-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="73888-126">WebApp Object</span></span>

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

### <span data-ttu-id="73888-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73888-127">CommonParameters</span></span>
<span data-ttu-id="73888-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73888-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73888-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73888-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73888-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73888-130">INPUTS</span></span>

### <span data-ttu-id="73888-131">System. String</span><span class="sxs-lookup"><span data-stu-id="73888-131">System.String</span></span>

### <span data-ttu-id="73888-132">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="73888-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="73888-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73888-133">OUTPUTS</span></span>

### <span data-ttu-id="73888-134">System. String</span><span class="sxs-lookup"><span data-stu-id="73888-134">System.String</span></span>

## <span data-ttu-id="73888-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73888-135">NOTES</span></span>

## <span data-ttu-id="73888-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73888-136">RELATED LINKS</span></span>

[<span data-ttu-id="73888-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="73888-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="73888-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="73888-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


