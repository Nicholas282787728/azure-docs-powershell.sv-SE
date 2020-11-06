---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578508"
---
# <span data-ttu-id="90ffe-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="90ffe-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="90ffe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="90ffe-103">Registrerar behållaren med ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="90ffe-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90ffe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90ffe-104">SYNTAX</span></span>

### <span data-ttu-id="90ffe-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="90ffe-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90ffe-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="90ffe-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ffe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90ffe-107">DESCRIPTION</span></span>
<span data-ttu-id="90ffe-108">**Register-AzureRmBackupContainer** cmdlet registrerar behållaren med ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="90ffe-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="90ffe-109">Om du vill konfigurera säkerhets kopiering med Azure Backup måste du först registrera din server eller virtuella dator med ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="90ffe-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="90ffe-110">Denna cmdlet registrerar en infrastruktur som en tjänst (IaaS) med det angivna valvet.</span><span class="sxs-lookup"><span data-stu-id="90ffe-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="90ffe-111">Registrerings åtgärden associerar den virtuella Azure-datorn med säkerhets kopierings valvet och spårar den virtuella datorn genom säkerhets kopierings cykeln.</span><span class="sxs-lookup"><span data-stu-id="90ffe-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="90ffe-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90ffe-112">EXAMPLES</span></span>

### <span data-ttu-id="90ffe-113">Exempel 1: registrera en virtuell dator i ett säkerhets kopierings valv</span><span class="sxs-lookup"><span data-stu-id="90ffe-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="90ffe-114">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ffe-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="90ffe-115">Kommandot lagrar valvet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="90ffe-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="90ffe-116">Det andra kommandot registrerar den virtuella datorn med namnet Contoso03Vm med valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="90ffe-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="90ffe-117">Den virtuella datorn tillhör tjänsten ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="90ffe-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="90ffe-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90ffe-118">PARAMETERS</span></span>

### <span data-ttu-id="90ffe-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="90ffe-119">-Name</span></span>
<span data-ttu-id="90ffe-120">Anger namnet på den virtuella dator som denna cmdlet registrerar.</span><span class="sxs-lookup"><span data-stu-id="90ffe-120">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ffe-121">-ResourceGroupName</span></span>
<span data-ttu-id="90ffe-122">Anger namnet på resurs gruppen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="90ffe-122">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffe-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90ffe-123">-ServiceName</span></span>
<span data-ttu-id="90ffe-124">Anger tjänst namnet på den virtuella dator som denna cmdlet registrerar.</span><span class="sxs-lookup"><span data-stu-id="90ffe-124">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="90ffe-125">Vanligt vis har ett moln tjänst namn ett suffix. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="90ffe-125">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="90ffe-126">Ta inte med suffixet när du anger den här parametern.</span><span class="sxs-lookup"><span data-stu-id="90ffe-126">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="90ffe-127">Använd Get-AzureRMVM cmdlet för att få information om en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="90ffe-127">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="90ffe-128">Tjänstens namn är egenskapen **DeploymentName** för den virtuella datorns objekt.</span><span class="sxs-lookup"><span data-stu-id="90ffe-128">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffe-129">-Valv</span><span class="sxs-lookup"><span data-stu-id="90ffe-129">-Vault</span></span>
<span data-ttu-id="90ffe-130">Anger det säkerhets kopierings valv som denna cmdlet registrerar virtuell dator med.</span><span class="sxs-lookup"><span data-stu-id="90ffe-130">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="90ffe-131">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="90ffe-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90ffe-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ffe-132">-DefaultProfile</span></span>
<span data-ttu-id="90ffe-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90ffe-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90ffe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ffe-134">CommonParameters</span></span>
<span data-ttu-id="90ffe-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ffe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ffe-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ffe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ffe-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90ffe-137">INPUTS</span></span>

### <span data-ttu-id="90ffe-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="90ffe-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="90ffe-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90ffe-139">OUTPUTS</span></span>

### <span data-ttu-id="90ffe-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="90ffe-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="90ffe-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90ffe-141">NOTES</span></span>

## <span data-ttu-id="90ffe-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90ffe-142">RELATED LINKS</span></span>

[<span data-ttu-id="90ffe-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="90ffe-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


