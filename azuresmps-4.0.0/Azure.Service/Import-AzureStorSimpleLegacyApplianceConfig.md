---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099489"
---
# <span data-ttu-id="84cc4-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="84cc4-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="84cc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="84cc4-103">Importerar en konfigurations fil.</span><span class="sxs-lookup"><span data-stu-id="84cc4-103">Imports a configuration file.</span></span>

## <span data-ttu-id="84cc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84cc4-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84cc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="84cc4-106">Cmdleten **import-AzureStorSimpleLegacyApplianceConfig** importerar konfigurations filen från den gamla produkten.</span><span class="sxs-lookup"><span data-stu-id="84cc4-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="84cc4-107">Filen innehåller information om volym behållare, säkerhets kopierings principer och autentiseringsuppgifter för lagrings konton för Azure StorSimple-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="84cc4-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="84cc4-108">Denna cmdlet returnerar den gamla enhetens konfigurations-metadata.</span><span class="sxs-lookup"><span data-stu-id="84cc4-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="84cc4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84cc4-109">EXAMPLES</span></span>

### <span data-ttu-id="84cc4-110">Exempel 1: importera en konfigurations fil</span><span class="sxs-lookup"><span data-stu-id="84cc4-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="84cc4-111">Det här kommandot importerar konfigurations filen på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="84cc4-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="84cc4-112">Kommandot inkluderar knappen för att dekryptera filen.</span><span class="sxs-lookup"><span data-stu-id="84cc4-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="84cc4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84cc4-113">PARAMETERS</span></span>

### <span data-ttu-id="84cc4-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="84cc4-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="84cc4-115">Anger dekrypteringsnyckeln för konfigurationen av den äldre apparaten.</span><span class="sxs-lookup"><span data-stu-id="84cc4-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cc4-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="84cc4-116">-ConfigFilePath</span></span>
<span data-ttu-id="84cc4-117">Anger den absoluta sökvägen till konfigurations filen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="84cc4-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cc4-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="84cc4-118">-Profile</span></span>
<span data-ttu-id="84cc4-119">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="84cc4-119">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cc4-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="84cc4-120">-TargetDeviceName</span></span>
<span data-ttu-id="84cc4-121">Anger namnet på mål enheten som presenteras i portalen.</span><span class="sxs-lookup"><span data-stu-id="84cc4-121">Specifies the name of the target device as presented in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84cc4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cc4-122">CommonParameters</span></span>
<span data-ttu-id="84cc4-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84cc4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cc4-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84cc4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cc4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84cc4-125">INPUTS</span></span>

### <span data-ttu-id="84cc4-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="84cc4-126">None</span></span>

## <span data-ttu-id="84cc4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84cc4-127">OUTPUTS</span></span>

### <span data-ttu-id="84cc4-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="84cc4-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="84cc4-129">Denna cmdlet returnerar information om konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="84cc4-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="84cc4-130">**LegacyApplianceConfiguration** -objektet innehåller följande information: konfigurations-ID, volym behållar namn, åtkomst kontroll poster, säkerhets kopierings principer, volym behållarna, lagrings konto uppgifter och volymer.</span><span class="sxs-lookup"><span data-stu-id="84cc4-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="84cc4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84cc4-131">NOTES</span></span>

## <span data-ttu-id="84cc4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84cc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="84cc4-133">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="84cc4-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


