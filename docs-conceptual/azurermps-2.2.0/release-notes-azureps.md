---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="8946a-103">Viktig information</span><span class="sxs-lookup"><span data-stu-id="8946a-103">Release notes</span></span>

<span data-ttu-id="8946a-104">Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.</span><span class="sxs-lookup"><span data-stu-id="8946a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="8946a-105">Version 2.2.0</span><span class="sxs-lookup"><span data-stu-id="8946a-105">Version 2.2.0</span></span>
* <span data-ttu-id="8946a-106">Compute</span><span class="sxs-lookup"><span data-stu-id="8946a-106">Compute</span></span>
  - <span data-ttu-id="8946a-107">Stöd för frågor om krypteringsstatus från tillägget AzureDiskEncryptionForLinux har lagts till</span><span class="sxs-lookup"><span data-stu-id="8946a-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="8946a-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="8946a-108">DataFactory</span></span>
  - <span data-ttu-id="8946a-109">Ny cmdlet för att visa aktivitetsfönster har lagts till</span><span class="sxs-lookup"><span data-stu-id="8946a-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="8946a-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="8946a-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="8946a-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="8946a-111">DataLake</span></span>
  - <span data-ttu-id="8946a-112">Parametern `Host` har ändrats till `DatabaseHost` och alias har lagts till för `Host`</span><span class="sxs-lookup"><span data-stu-id="8946a-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="8946a-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="8946a-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="8946a-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="8946a-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="8946a-115">Stöd för borttagning av ACL och standard-ACL har lagts till</span><span class="sxs-lookup"><span data-stu-id="8946a-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="8946a-116">Stöd för att hämta och ange ej namngivna behörigheter för filer och mappar har lagts till</span><span class="sxs-lookup"><span data-stu-id="8946a-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="8946a-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8946a-117">KeyVault</span></span>
  - <span data-ttu-id="8946a-118">Stöd för certifikat har lagts till</span><span class="sxs-lookup"><span data-stu-id="8946a-118">Add support for certificates</span></span>
    + <span data-ttu-id="8946a-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8946a-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="8946a-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8946a-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="8946a-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8946a-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="8946a-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8946a-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="8946a-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8946a-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="8946a-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="8946a-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="8946a-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="8946a-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8946a-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="8946a-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="8946a-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="8946a-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="8946a-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="8946a-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="8946a-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8946a-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="8946a-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8946a-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="8946a-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8946a-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="8946a-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="8946a-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="8946a-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="8946a-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="8946a-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8946a-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="8946a-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="8946a-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="8946a-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="8946a-138">Nätverk</span><span class="sxs-lookup"><span data-stu-id="8946a-138">Network</span></span>

  - <span data-ttu-id="8946a-139">Ny switchparameter har lagts till för nätverksgränssnittet för att aktivera/inaktivera accelererat nätverk +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="8946a-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="8946a-140">PowerShell-cmdletar för att aktivera gateway-funktionen aktiv-aktiv</span><span class="sxs-lookup"><span data-stu-id="8946a-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="8946a-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="8946a-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="8946a-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="8946a-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="8946a-143">Ny cmdlet har lagts till</span><span class="sxs-lookup"><span data-stu-id="8946a-143">Added new cmdlet</span></span>
    + <span data-ttu-id="8946a-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="8946a-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="8946a-145">Resurser</span><span class="sxs-lookup"><span data-stu-id="8946a-145">Resources</span></span>
  - <span data-ttu-id="8946a-146">Stöd för zoner i provider- och resurs-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8946a-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="8946a-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="8946a-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="8946a-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8946a-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="8946a-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8946a-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="8946a-150">SQL</span><span class="sxs-lookup"><span data-stu-id="8946a-150">Sql</span></span>
  - <span data-ttu-id="8946a-151">Nya cmdletar har lagts till för principhantering av Azure SQL-hotidentifiering på servernivå</span><span class="sxs-lookup"><span data-stu-id="8946a-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="8946a-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="8946a-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="8946a-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="8946a-155">Nya cmdletar har lagts till för aktivera/inaktivera GeoBackupPolicy för Sql Azure DataWarehouses</span><span class="sxs-lookup"><span data-stu-id="8946a-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="8946a-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="8946a-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="8946a-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="8946a-158">Nya cmdletar har lagts till för Azure SQL Advisors och för API:er för rekommenderade åtgärder</span><span class="sxs-lookup"><span data-stu-id="8946a-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="8946a-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="8946a-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="8946a-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="8946a-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="8946a-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="8946a-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="8946a-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="8946a-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="8946a-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="8946a-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="8946a-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="8946a-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="8946a-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8946a-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="8946a-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8946a-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="8946a-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8946a-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="8946a-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="8946a-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="8946a-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="8946a-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="8946a-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="8946a-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
