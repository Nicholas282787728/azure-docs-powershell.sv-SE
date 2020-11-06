---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582032"
---
# <span data-ttu-id="7c7f1-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c7f1-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="7c7f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7f1-103">Hämtar en lista över återställnings tjänstens valv.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c7f1-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c7f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c7f1-105">DESCRIPTION</span></span>
<span data-ttu-id="7c7f1-106">Cmdleten **Get-AzureRmRecoveryServicesVault** hämtar en lista över återställnings tjänst valv i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="7c7f1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="7c7f1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c7f1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="7c7f1-109">Hämta listan med valv i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="7c7f1-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7c7f1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="7c7f1-111">Hämta listan med valv i resurs gruppen i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="7c7f1-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7c7f1-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="7c7f1-113">Hämta valvet i resurs gruppen med angivet namn.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="7c7f1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c7f1-114">PARAMETERS</span></span>

### <span data-ttu-id="7c7f1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c7f1-115">-Name</span></span>
<span data-ttu-id="7c7f1-116">Anger namnet på valvet du vill fråga efter.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c7f1-118">Anger namnet på den Azure-adressresurs som du vill skapa eller från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7f1-119">-DefaultProfile</span></span>
<span data-ttu-id="7c7f1-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c7f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7f1-121">CommonParameters</span></span>
<span data-ttu-id="7c7f1-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7f1-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7f1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7f1-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c7f1-124">INPUTS</span></span>

### <span data-ttu-id="7c7f1-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="7c7f1-125">None</span></span>
<span data-ttu-id="7c7f1-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7c7f1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c7f1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c7f1-127">OUTPUTS</span></span>

### <span data-ttu-id="7c7f1-128">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="7c7f1-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="7c7f1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c7f1-129">NOTES</span></span>

## <span data-ttu-id="7c7f1-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c7f1-130">RELATED LINKS</span></span>

[<span data-ttu-id="7c7f1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7c7f1-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7c7f1-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c7f1-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7c7f1-133">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7c7f1-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


