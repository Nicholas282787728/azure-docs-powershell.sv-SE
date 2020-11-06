---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572559"
---
# <span data-ttu-id="362bb-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="362bb-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="362bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="362bb-102">SYNOPSIS</span></span>
<span data-ttu-id="362bb-103">Hämtar en Azure Web App slot-publicerings profil.</span><span class="sxs-lookup"><span data-stu-id="362bb-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="362bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="362bb-104">SYNTAX</span></span>

### <span data-ttu-id="362bb-105">S</span><span class="sxs-lookup"><span data-stu-id="362bb-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="362bb-106">S2</span><span class="sxs-lookup"><span data-stu-id="362bb-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="362bb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="362bb-107">DESCRIPTION</span></span>
<span data-ttu-id="362bb-108">Cmdleten **Get-AzureRmWebAppSlotPublishingProfile** hämtar webb program publicerings profilen för den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="362bb-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="362bb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="362bb-109">EXAMPLES</span></span>

### <span data-ttu-id="362bb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="362bb-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="362bb-111">Det här kommandot får publicerings profilen i FTP-format för fack Slot001 som hör till Web App-ContosoWebApp som är kopplat till resurs gruppens standard-väst och lagrar den i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="362bb-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="362bb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="362bb-112">PARAMETERS</span></span>

### <span data-ttu-id="362bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362bb-113">-DefaultProfile</span></span>
<span data-ttu-id="362bb-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="362bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="362bb-115">-Format</span><span class="sxs-lookup"><span data-stu-id="362bb-115">-Format</span></span>
<span data-ttu-id="362bb-116">Format</span><span class="sxs-lookup"><span data-stu-id="362bb-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362bb-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="362bb-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="362bb-118">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="362bb-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="362bb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="362bb-119">-Name</span></span>
<span data-ttu-id="362bb-120">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="362bb-120">WebApp Name</span></span>

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

### <span data-ttu-id="362bb-121">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="362bb-121">-OutputFile</span></span>
<span data-ttu-id="362bb-122">Utdatafil</span><span class="sxs-lookup"><span data-stu-id="362bb-122">Output File</span></span>

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

### <span data-ttu-id="362bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="362bb-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="362bb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="362bb-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="362bb-125">-Slot</span></span>
<span data-ttu-id="362bb-126">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="362bb-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362bb-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="362bb-127">-WebApp</span></span>
<span data-ttu-id="362bb-128">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="362bb-128">WebApp Object</span></span>

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

### <span data-ttu-id="362bb-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="362bb-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="362bb-130">Inkludera slut punkter för återställning av katastrof om sant</span><span class="sxs-lookup"><span data-stu-id="362bb-130">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="362bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362bb-131">CommonParameters</span></span>
<span data-ttu-id="362bb-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362bb-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="362bb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362bb-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="362bb-134">INPUTS</span></span>

### <span data-ttu-id="362bb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="362bb-135">System.String</span></span>

### <span data-ttu-id="362bb-136">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="362bb-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="362bb-137">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="362bb-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="362bb-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="362bb-138">OUTPUTS</span></span>

### <span data-ttu-id="362bb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="362bb-139">System.String</span></span>

## <span data-ttu-id="362bb-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="362bb-140">NOTES</span></span>

## <span data-ttu-id="362bb-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="362bb-141">RELATED LINKS</span></span>

[<span data-ttu-id="362bb-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="362bb-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="362bb-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="362bb-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="362bb-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="362bb-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
