---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 58d15476921005b6da674d6a16441eb2e4f82865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578580"
---
# <span data-ttu-id="77656-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="77656-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="77656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77656-102">SYNOPSIS</span></span>
<span data-ttu-id="77656-103">Skapar MOF-filer för meta-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="77656-103">Creates meta-configuration .mof files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77656-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77656-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77656-105">DESCRIPTION</span></span>
<span data-ttu-id="77656-106">Cmdleten **Get-AzureRmAutomationDscOnboardingMetaconfig** skapar APS-MOF-filer (Managed Object Format) för AP (för önskat tillstånd).</span><span class="sxs-lookup"><span data-stu-id="77656-106">The **Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="77656-107">Denna cmdlet skapar en. MOF-fil för varje dator namn som du anger.</span><span class="sxs-lookup"><span data-stu-id="77656-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="77656-108">Cmdleten skapar en mapp för MOF-filerna.</span><span class="sxs-lookup"><span data-stu-id="77656-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="77656-109">Du kan köra cmdleten Set-DscLocalConfigurationManager för den här mappen om du vill att dessa datorer ska finnas i ett Azure Automation-konto som DSC-noder.</span><span class="sxs-lookup"><span data-stu-id="77656-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="77656-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77656-110">EXAMPLES</span></span>

### <span data-ttu-id="77656-111">Exempel 1: inbyggda servrar i Automation DSC</span><span class="sxs-lookup"><span data-stu-id="77656-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="77656-112">Det första kommandot skapar DSC meta-konfigurationsfiler för två servrar för det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="77656-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="77656-113">Kommandot sparar dessa filer på Skriv bordet.</span><span class="sxs-lookup"><span data-stu-id="77656-113">The command saves these files on a desktop.</span></span>

<span data-ttu-id="77656-114">I det andra kommandot används cmdleten **set-DscLocalConfigurationManager** för att tillämpa meta-konfigurationen på de angivna datorerna som DSC-noder.</span><span class="sxs-lookup"><span data-stu-id="77656-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="77656-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77656-115">PARAMETERS</span></span>

### <span data-ttu-id="77656-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77656-116">-AutomationAccountName</span></span>
<span data-ttu-id="77656-117">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="77656-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="77656-118">Du kan välja de datorer som parametern *computername* ska ange för det konto som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="77656-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77656-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="77656-119">-ComputerName</span></span>
<span data-ttu-id="77656-120">Anger en matris med namn på datorer som denna cmdlet genererar. MOF-filer för.</span><span class="sxs-lookup"><span data-stu-id="77656-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="77656-121">Om du inte anger den här parametern genererar cmdleten en. MOF-fil för den aktuella datorn (localhost).</span><span class="sxs-lookup"><span data-stu-id="77656-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77656-122">-Force</span><span class="sxs-lookup"><span data-stu-id="77656-122">-Force</span></span>
<span data-ttu-id="77656-123">Tvingar kommandot att köras utan att du behöver bekräfta och ersätta befintliga MOF-filer med samma namn.</span><span class="sxs-lookup"><span data-stu-id="77656-123">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="77656-124">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="77656-124">-OutputFolder</span></span>
<span data-ttu-id="77656-125">Anger namnet på en mapp där denna cmdlet lagrar. MOF-filer.</span><span class="sxs-lookup"><span data-stu-id="77656-125">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77656-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77656-126">-ResourceGroupName</span></span>
<span data-ttu-id="77656-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="77656-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="77656-128">Denna cmdlet skapar. MOF-filer till inbyggda datorer i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="77656-128">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77656-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77656-129">-Confirm</span></span>
<span data-ttu-id="77656-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77656-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77656-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77656-131">-WhatIf</span></span>
<span data-ttu-id="77656-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77656-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77656-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77656-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77656-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77656-134">-DefaultProfile</span></span>
<span data-ttu-id="77656-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77656-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77656-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77656-136">CommonParameters</span></span>
<span data-ttu-id="77656-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77656-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77656-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77656-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77656-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77656-139">INPUTS</span></span>

## <span data-ttu-id="77656-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77656-140">OUTPUTS</span></span>

### <span data-ttu-id="77656-141">Microsoft. Azure. commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="77656-141">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="77656-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77656-142">NOTES</span></span>

## <span data-ttu-id="77656-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77656-143">RELATED LINKS</span></span>

